<!--
.. date: 2024-07-26
.. tags: cleantech, startups, career
-->

# Energy Tech Data Problems

The intersection of climate technology and data has never been more critical. We have more data than ever to work with, and climate challenges are more pressing than ever. But climate tech is not a monolith, and exactly what data work looks like varies by sector. I'm most excited about [the energy side of climate tech](../rocket_ships/), and break it down further into 4 categories: [Efficiency](#efficiency), [Renewables](#renewables), [Electrification](#electrification), and [Grid Modernization](#grid-modernization). I also think about [Picks & Shovels](#picks-and-shovels). The businesses in each of these five categories have different types of data needs.

 This understanding of the space was key to the decision I made to join Palmetto, and I hope it helps others make their choices too. Working on climate is fundamentally valuable, and probably puts you on a team with great people. Working on problems that interest you, that harness your best abilities, is even better.

## Efficiency 
Energy efficiency means, simply, using less energy. On its surface, it's sensible: if we use less energy, we don't need to burn as many fossil fuels. Companies in this space are developing less resource-intensive manufacturing processes ([37% of global energy use](https://www.iea.org/energy-system/industry)), building materials that better insulate and take advantage of the natural environment to reduce requirements for heating and cooling ([almost 25% of energy use worldwide](https://www.iea.org/reports/global-status-report-for-buildings-and-construction-2019)), and devices and appliances that use less energy, . They are also optimally routing traffic and goods to conserve fuel ([also about 25% of energy use worldwide](https://www.eia.gov/outlooks/ieo/pdf/transportation.pdf)) and nudging individuals to take energy-efficient actions. [[1]](#1)

Improving the efficiency of manufacturing processes and developing novel materials are deep tech problems. I've found over the years that it's a lot easier to [take a deep tech scientist and throw them at data science](https://insightfellows.com/?utm_source=linkedin&utm_medium=main_page) than it is to take a data scientist and make them a deep tech specialist, so until companies working on these solutions reach large scale, data support tends to come from flexible scientists and engineers rather than dedicated data folks. The roles I do see index heavily on BI and business analytics at first. Rarely will such a startup build a central data team, but rather embed people directly in to other organizations.

Companies developing efficient devices similarly don't need many data folks in the early days, but when they start bringing their products to market, classic data problems behind sales and servicing bring analysts and scientists onto the team, supported by data engineers.

Companies focused on efficient routing, of course, are built around data scientists/machine learning engineers with expertise in scalable optimization. Real-time object detection and tracking experts as well as autonomous vehicle technologists are important to this field, too [[2]](#2). Some companies will look for engineers more than scientists, but the line between titles is blurry in these spaces. 

Finally, [my least favorite category](../../pages/snippets/humility_is_key_to_growth/): behavioral nudging. Residential energy use makes up about 25% of global energy consumption, but much of that is structural, not behavioral. We build inefficient homes full of inefficient appliances, and then ask people to bear the burden of turning their thermostats down on hot days so that a chemical plant can keep chugging out plastics. Yes, I spent ~3 years pioneering this field at Opower. I learned a lot, and the DE, DS, ML, and analytics problems were fun: developing insights using energy data, employing classic behavioral science methods using engagement data, and measuring the impact of interventions with statistical tests. This type of work is now best suited, in my opinion, to nudging people to take higher-value actions, like buying efficient devices or using electricity from renewable sources. To wit...

## Renewables
Renewable energy sources allow us to use energy without burning fossil fuels. While coal, oil, and natural gas have provided easy-to-harness energy for decades, they are not only finite on our planet, but all together, their total volume on the earth can provide just 5% as much as solar energy alone could provide *in a single year*. [[3]](#3) More energy is available from the sun in an hour than humans currently use in a year (!), but we are still learning how to cost-effectively harness solar power. Over the last decade we've seen [dramatic increases in photvoltaic cell efficiency](https://www.nrel.gov/pv/cell-efficiency.html) [[4]](#4), and [costs have come down 10-fold over the same time](https://ourworldindata.org/cheap-renewables-growth). Other sources of renewable power (in order of available energy: wind, biomass, hydro, geothermal, wave, tidal, and biomass), though much less prevalent than solar, are still capable of providing more than double the world's current energy demand. [The world has made great strides in recent years toward harnessing renewables broadly](https://ourworldindata.org/renewable-energy) — [even the US is getting 20% of our energy from renewables as of 2023](https://www.eia.gov/tools/faqs/faq.php?id=427&t=3) — but so much opportunity is on the table. 

Again, some of the problems here are deep tech problems: specific training is typically required to develop novel materials, manufacturing approaches, and other innovations that make renewable power generation more productive. But the ["soft costs" attached to these hard technologies can make up more than half of the total cost to bring projects to life](https://www.energy.gov/eere/solar/solar-soft-costs-basics): sales/GTM, optimizing installation designs, improving speed and quality of the installation process, financing, monitoring, and proactively servicing. Data roles can play an important role in solving all of these problems, and often require [teams of data practitioners with different skillsets](../../pages/snippets/build_teams_of_t_shapes/) to come together to accomplish doing so. 


## Electrification
With more renewable electricity sources, it's easier to use fewer hydrocarbons by going all-electric. A person living in an all-electric house powered by solar, driving an electric vehicle (EV), may live almost entirely off grid. [Electrify everything](https://homes.rewiringamerica.org/) means developing electric-powered devices where we once relied on coal or natural gas or oil, and it also means convincing people and businesses to use them [[5]](#5).

Achieving this goal requires inventing, building, and marketing new devices like electric vehicles and heat pumps. Again, data roles are crucial in classic applications of product development, manufacturing, sales, and maintenance. In the case of EVs, a robust charging network is also critical to drive adoption: data science approaches are key in optimizing placement, number, and size of these installations.

Data also plays a vital role in helping consumers of all sizes, from residential to commercial/industrial, understand the impact of electrification on their energy bills. Putting trustworthy data in people's hands is key to helping them make informed decisions, which will drive adoption of new technologies. These types of tools are a classic type of data product, and so may even be overseen by a data product manager.

## Grid modernization
["The grid of tomorrow doesn’t look like an industrial supply chain. It looks like the internet."](https://medium.com/@EqualVentures/the-new-energy-economy-44aa33b6b7ba) As we see more installations of renewable energy sources and greater use of electricity, the grid must evolve to deliver power to different places at different times than in years past. On top of that, as bidirectional inverters allow increasingly prevalent distributed energy resources (DERs, e.g. installations of renewable energy sources and storage devices) to discharge to the grid, there arises an opportunity to take advantage of power sources that look nothing like traditional power plants. 

Data problems in this space lean heavily toward forecasting, simulation and optimization. If we can reliably predict how demand will shift and where new DERs will come online, we can build simulations of the grid that accurately mirror the world we'll live in, and then optimize when and where we store, discharge, sell, and use power. Such work has always been critical for utilities, but the primary decision resulting from such analysis has historically been "when and where do we need to build another power plant, and how big does it need to be?" Now, with the advent of new technologies, the number of questions to answer explodes: which demand response programs should we implement? Should we develop a large-scale renewable project? Can we take an old, inefficient, dirty power plant offline? [[6]](#6)

These problems exist also at a smaller scale, with homeowners and building managers running "[microgrid](https://www.nrel.gov/grid/microgrids.html#:~:text=A%20microgrid%20is%20a%20group,grid%2Dconnected%20or%20island%20mode.)" software to do the same within their walls. 

## Picks and Shovels
In addition to the 4 categories I talked through here, there are a huge number of companies developing tooling that climate tech companies rely on to succeed. Some of this is generic SaaS: at Palmetto, for instance, we've stood up a classic "modern data stack" of third-party tools. But there are also companies and research organizations developing climate-tech-specific data sources, APIs, and applications. Arcadia's acquisition of [Genability](https://www.genability.com/) has made them a reliable cornerstone of energy data infrastructure. 
I'm excited to see what [Texture](https://www.texturehq.com/) does here, too — their aim is to be "Plaid for energy." [Pencil](https://www.pencilenergy.com/) and [Fordje](https://www.fordje.com/) aim to make it easier for climate tech companies to keep track of relevant regulations, which vary enormously by jurisdiction and change regularly. These types of companies very likely hire for some of the most interesting data engineering jobs I've mentioned so far.

Research labs, government institutions, nonprofits, and universities also develop technologies and datasets that are crucial to so much of what we build. Researchers at these institutions tend to develop the deepest knowledge in the field, and as a result are well-connected throughout the industry. 

A final note: for-profit enterprises don't just work with the types of companies in this picks and shovels group. The energy space of today is highly collaborative. A solution in one area may require a partner doing totally different work to be fully realized. Wherever you plug in (_I had to!_), you're sure to learn about a wide swath of things discussed here. 


# Feedback

What did I miss? [Get in touch.](mailto:emilypastewka@gmail.com)

---

This post is part of a series: [Back to My Roots in Cleantech](../back_to_my_roots_in_cleantech/)

---

#### [1]
It's tempting to put the sharing economy in this bucket. When I joined Uber, for example, I thought ridesharing would make car transit more efficient, but that didn't quite pan out. Similarly, Rent the Runway was a bet on reducing the impact of fast fashion, but investor demands made the double bottom line hard to hold — ultimately, we wanted people to conform to the cycles of fashion and buy, buy, buy. The sharing economy may be a better bet, but because it still follows the core tenets of consumerism, I remain skeptical here, too. I'm therefore omitting these spaces from the main text. If you believe there is still a path forward, you may be right, I may just be jaded.

#### [2]
I had a lot of fun working on [smart cities](https://www.cosmos-lab.org/experimentation/smart-city-intersections/) in grad school. The pace of tangible application was a little too slow for me to commit to the space full-time. Even autonomous vehicles are far behind expected schedule. But I'm bullish in the long run.

#### [3]
All the stats in this section come from the [CU Boulder Coursera on Renewable Energy Technology Fundamentals](https://www.coursera.org/learn/renewable-energy-technology-fundamentals/home/module/1). It's very focused on hard science. I highly recommend it. 

#### [4]
An argument exists that we may soon be hitting a [limit](https://ph.qmul.ac.uk/sites/default/files/u75/Solar%20cells_environmental%20impact.pdf) on the potential for current technologies to convert the sun's rays into electricity, but this has recently been [empirically disproven](https://www.nrel.gov/pv/cell-efficiency.html), at least at small scale. 

#### [5]
The animated data visualization near the top of [this NYT article](https://www.nytimes.com/interactive/2023/04/14/climate/electric-car-heater-everything.html) does a great job of showing where there is room left to run in electrifying US energy usage. Rewiring America's [Pace of Progress report](https://www.rewiringamerica.org/pace) is even more detailed.

#### [6]
You didn't ask for a 116 page paper on this but it's probably the sexiest thing happening in climate tech, so [here you go](https://iea.blob.core.windows.net/assets/3520710c-c828-4001-911c-ae78b645ce67/UnlockingthePotentialofDERs_Powersystemopportunitiesandbestpractices.pdf).

More consumable: podcasts and newletters from the [DER Task Force](https://www.dertaskforce.com/).