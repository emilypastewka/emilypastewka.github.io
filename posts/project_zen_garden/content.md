<!--
.. date: 2026-02-13
.. tags: 
-->

# Project Zen Garden

It feels wild to be writing about my last job from within my current reality, leading data science teams at Anthropic. But good ideas don't go away — we've just got new tools with which to make them into reality. 

I'll describe the situation in 2023 and what I did about it.

## The Promise and Peril of Data Democratization

I self-select into jobs where I get to have a big impact. And as much as I like to build, I also like to fix things. Never have I started a job where I heard, "everything is in great shape, your job is just to keep it that way." 

When I started at Palmetto, I heard phrases like "nobody trusts our data" from stakeholders. At the same time, I dug in to the technical work the team had done and found it was solid across many domains. Internal and external data sources flowed reliably into Snowflake via Fivetran and Stitch. We had a good medallion architecture set up with dbt. Our airflow dags ran quickly, and alerted effectively when they had issues. 

The problem turned out to be Looker. Palmetto, as many companies, embraced the concept of data democratization, but the governance was missing. 

We used Looker as our semantic layer.

But here's what happens next, and I've now seen this pattern at multiple companies: the Garden of Eden becomes overgrown.
People start building reports on top of raw data because the modeled data doesn't have quite the field they need. Someone creates a dashboard for a one-time analysis and it becomes the de facto source for a key metric. Different teams develop different definitions of the same concept. A developer creates an experimental data model in a sandbox environment, and six months later, mission-critical business processes depend on it.
Wrong answers based on faulty data lead to costly mistakes. [TKTK: add 1-2 concrete examples of decisions made on bad data]. Multiple definitions of the same metric lead to swirling, unproductive conversations instead of facilitating quick decisions. Trust erodes. People start second-guessing the numbers. Meetings devolve into arguing about whose dashboard is "right."
The data team knows the validated models exist, but users don't know which assets are trustworthy and which aren't. The search results are clogged with abandoned experiments. The beautiful self-serve vision has become a liability.
Recognizing the Problem at Palmetto
At Palmetto, we enabled small teams to move fast through single-threaded ownership of clear objectives in a matrix organization. Data was supposed to be the toolset that gave all leaders a common language. To remain nimble while basing decisions on first principles, teams needed access to data that was 100% reliable and easy to work with.
Our data architecture looked like this: Looker sat on top of Snowflake, our data warehouse, which contained a mix of raw and modeled data. Raw data came directly from upstream sources—internal systems or external services like Stripe. We transformed raw data into clean, usable models through careful work: filtering out test cases and duplicates, extracting information from complex logs, ensuring tables could join cleanly with consistent time zones and naming conventions.
Once modeled, data was shipped to Looker, where our validated data models were supposed to enable anyone to confidently find answers. The philosophy was simple: we (the data team) go slow 🐢 so that you (the end users) can go fast ⚡️!
But we had a problem called Sandbox.
Sandbox was a Looker workspace that gave power users access to all of Palmetto's data—modeled and unmodeled, validated and unvalidated. It had been created years earlier as a temporary solution during a major platform migration, enabling intrepid users to work with raw data while the data team played catch-up. It was never meant to be permanent.
But Sandbox had existed so long that working fully out of Sandbox had become normalized. When I looked at our metrics, I found dashboards powering key business processes sitting on top of unvalidated data. We were tracking [TKTK: add specific number or percentage] of our BI queries running against Sandbox instead of validated production explores.
We had built a beautiful validated data layer, but nobody was using it. Our entire business was at risk.
Project Zen Garden: Pruning the Overgrowth
I called the initiative to fix this Project Zen Garden. The name was deliberate—this wasn't about burning everything down and starting over. It was about careful cultivation: pruning away the overgrowth, creating clear paths through the garden, and establishing what belonged where.
Our north star metric was simple: 90% of queries running on production explores (i.e., not Sandbox). This would ensure the vast majority of BI was based on single source of truth data assets, while leaving space for individuals to test out new data assets before they were permanently modeled. Over time, as our processes scaled and we could model new data assets more quickly, we might increase this target from "one nine" to "two nines."
The strategy had six components:
1. Ensure Your Source of Truth Is Actually Comprehensive
The validated data layer can't become the default if it doesn't contain everything people need. This sounds obvious, but it's where many data teams fail. They build beautiful core models and wonder why people keep going around them to raw data.
We audited what people were actually building in Sandbox and identified the gaps. The priorities were:
Core business reporting needs:

Goals and pacing data
A new sales explore that started from leads (not just closed deals)
Integration of data from our newer systems into our primary validated models
Post-fulfillment data with support cases and production metrics

[TKTK: add detail on how we prioritized these - was it based on query volume? stakeholder interviews? both?]
This work happened in the background throughout the rest of the project. There's no point in restricting access to Sandbox if people genuinely can't do their jobs without it.
2. Make Trust Visible at a Glance
As of November 2023, we had 814 dashboards (up 22% from just the prior quarter) and 1,254 looks (up 28% from the previous quarter). The majority of these lived outside of any organized folder structure.
The problem wasn't just volume—it was that validated, high-quality assets were drowning in a sea of one-off analyses, abandoned experiments, and duplicative reports. Even if someone wanted to use the right data, they couldn't easily find it.
We tackled this through several parallel efforts:
Removing cruft: Looker has good search functionality, but only if useful content rises to the top. We systematically deleted unused content. [TKTK: add criteria for what counted as "unused" - 90 days no views? longer?]
Reorganizing folders: We created a clear structure that separated validated, source-of-truth assets from everything else:

Strategic dashboards answered "How is this business doing?" These rolled up to executive leadership and board reporting.
Operational dashboards answered "Where are projects getting stuck? Who needs coaching?" These supported day-to-day team management.

For each strategic dashboard, we established clear ownership—mostly the central data team, but with explicit tracking when teams outside of data owned key metrics.
Color-coding everything: This was the piece that really made the difference. We implemented a red/yellow/green coding system across all Looker assets—dashboards, looks, and even the underlying data views.

🟢 Green: Validated data models owned by the data team. Built on top of our carefully maintained marts. Documented. Trustworthy.
🟡 Yellow: Experimental or transitional. Might be built on validated data but the dashboard itself isn't maintained. Use with caution.
🔴 Red: Built on Sandbox or other unvalidated data sources. Do not use for decision-making.

We used the Looker API to automatically tag and color-code assets based on which explores and views they referenced. [TKTK: add specifics on the API calls used - was it the PATCH /dashboards/{id} endpoint? did you use tags or a different mechanism?]
The color coding showed up everywhere: in folder listings, in search results, in the dashboard header when viewing a report. It was impossible to miss.
3. Lock Down Personal Folders (Temporarily)
This was the most controversial move, and it needed to be.
Looker is meant to democratize data, but data is only valuable when it's trusted. We needed to change how people thought about what belonged in the public domain versus their personal workspace.
Using the Looker API, we changed sharing permissions so that users could still develop content, but they would be the only people able to view their own content by default. [TKTK: which permission level did we set - Viewer? Developer? What API calls specifically?]
To make something public, users needed to go through a formal promotion process. We created a simple form where they could request to publish a dashboard or look. The data team would review it to ensure:

It was built on validated data (green explores)
It wasn't duplicating existing reports
It was properly documented
It served a clear business need

This wasn't meant to be a permanent state—it was a pattern interrupt. We needed to break the muscle memory of "build in Sandbox, share with team, call it done."
4. Training and Communication
Once we had clean production data and clear pathways to find it, we needed to train people on the new system.
[TKTK: add details on training approach - was it company-wide sessions? team-by-team? what were the core topics covered?]
Key topics included:

What kind of work should I do in Looker versus other tools?
How do I find documentation for data models?
How do I navigate the new folder structure?
What do the colors mean and why should I care?
How do I request new data models or dashboard promotion?

5. Migrate Critical Sandbox Assets
Once we had color-coding in place, we needed to quickly reduce the prevalence of yellow and red assets. Otherwise, users would become inured to their existence—the warnings would lose meaning.
We worked with stakeholders to audit all shared dashboards and determine:

Is it still needed? Do other dashboards enable the same analysis?
If still needed, what are the dependencies for migration?
Who owns this and will maintain it going forward?

[TKTK: add number of dashboards migrated, timeline, any notable challenges]
This work didn't fall strictly on the data team. We made it clear: if you require the use of data, you de facto require the use of good data. Teams needed to partner with us on migration.
6. Automate Model-to-BI Pipeline
The long-term solution to preventing Sandbox sprawl was to reduce the time between "I need new data" and "that data is available in validated form."
We built automation to convert dbt models into Looker views on PR merge, using tools like dbt2looker. When a data engineer created a new mart in our dbt project, it would automatically:

Generate the corresponding Looker view with all columns and documentation
Join it into the appropriate explore(s)
Maintain perfect naming consistency between Snowflake tables and Looker views

Why this mattered:

Less dev time manually setting up Looker meant faster turnaround
Perfect match between Snowflake tables and Looker views (and their docs!) meant less time spinning trying to understand what's what
Reduced the temptation to "just quickly grab this from raw data" because the modeled version was available much faster

What we gave up:

Some Looker measures still needed manual creation—complex filtered aggregations, for instance
We lost some flexibility in how data was presented in Looker versus how it was modeled in the warehouse

What we required for success:

Only marts in our reports/ folder were exposed to Looker—these were specifically designed for end-user consumption
Core marts got merged into a small set of core explores rather than creating explore sprawl
Column names had to be identical across tables so Looker users could easily join data without custom tailoring
Documentation was required for all models and columns—we failed CI if it was missing
The automation code needed to be understandable and modifiable by the entire data team, not just one person

[TKTK: add details on the specific automation approach - was it a custom GitHub Action? dbt2looker out of the box? other tool?]
7. Further Disincentivize Sandbox Development
The previous steps made validated data easier to use. This step made unvalidated data harder to misuse.
We raised the bar for getting Looker developer permissions. Previously, we'd granted contributor access fairly liberally. Under the new system, users needed to complete training and demonstrate understanding of data governance principles. [TKTK: add specifics on what the training covered and what the vetting process looked like]
We also instituted regular Sandbox teardowns. Sandbox could continue to exist for truly experimental work, but experiments that became long-term needed to be migrated to validated models. To prevent any Sandbox work from accidentally becoming a source of truth, we scheduled quarterly cleanups where we'd archive or delete Sandbox content that was more than [TKTK: 90 days? 6 months?] old.
The simpler alternative would have been to delete Sandbox entirely, but we decided to keep it as a release valve for genuinely experimental analysis while making it very clear that it was temporary by design.
Results and Reflections
[TKTK: add outcomes - did you hit the 90% target? what was the timeline? what resistance did you face? what would you do differently?]
The broader lesson here isn't specific to Looker or Snowflake or dbt. It's about recognizing that data democratization and data governance aren't opposing forces—they're symbiotic.
Democratization without governance leads to chaos and eroded trust. Governance without democratization leads to bottlenecks and frustrated users. The sweet spot is making the right thing the easy thing: comprehensive validated data that's genuinely easier to use than going around it.
A few principles that mattered:
Go slow so others can go fast. The data team's job is to create leverage. Every hour we spent carefully modeling data and building automation saved dozens of hours across the organization.
Make trust visible. People can't choose trustworthy data if they can't identify it at a glance. Color-coding was simple but transformative.
Meet users where they are. We didn't just tell people "stop using Sandbox." We made sure validated data actually served their needs, then made it easy to find and use.
Automate the boring parts. The faster you can get validated data in front of people, the less they're tempted to work around you.
Temporary restrictions can create permanent change. Locking down personal folders wasn't meant to be forever, but it broke old habits and established new norms.
I find myself talking about this project frequently when data leaders ask me about scaling their teams. The specific tools change—at Anthropic, we're working with different systems and much larger scale—but the underlying challenge remains constant: how do you maintain a single source of truth while empowering everyone to work with data?