<!--
.. date: 2024-12-31
.. tags: startups, vc, pe
-->

# Data in the world of VC & PE

During my [wilderness year](../the_wilderness_year/), I toyed with the idea of going into finance. I had previously worked on the data science team that supported Uber's Finance org for more than 4 years, guiding how billions of dollars were invested 2016-2020, so recruiters had reached out frequently about roles at not just FinTech startups but banks, hedge funds, and private equity firms. Private equity (PE) and venture capital (VC) appeal to me in many ways: these firms work with large numbers of external companies, which can allow internal employees the chance to constantly learn new things. Because of how compensation works (especially at higher levels), people tend to stay for a long time, building close relationships. And there appears to be something of a new era for data having an impact on these companies, as there was in tech in the 2010s [[1]](#1).

When I started to seriously consider accepting a role leading the data org at a VC or PE firm [[2]](#2), I found there seem to be 3 common models.

## 3 common data roles in PE & VC
### 1 Informing investments
Putting data behind investment decisions is usually what people first think of when they think about data work at an investment firm. After all, don't [quants run Wall Street now](https://www.wsj.com/articles/the-quants-run-wall-street-now-1495389108)?

Trading is nothing like PE or VC. Using data & ML to drive alpha beyond the know-how of investors hailing from more traditional Finance backgrounds is pretty tough to do. Such models are typically built for the upper funnel, i.e. prioritizing known deal flow. As such, they are constrained by the deal flow available to feed in. On top of that, they are constrained by the data available, and firms that focus on early-stage companies don't have a lot of data to go on: many seed investors will admit that their decisions are largely bets on the founders. Though there may be some alpha to extract in data collected about founders, given the relatively small size of that data, it's not clear that an expensive data science project do much better at making those decisions than a human [[3]](#3). Later-stage investments come with a lot more data, but also a lot more nuance. Parameters and data relevant for opportunity A may be completely different than those relevant for opportunity B. 

<!-- On top of that, VC & PE are very relationship-based. Nobody — even tech investors — wants AI to steal their job. To that end, where I have heard of DS teams successfully building models to inform investments is far up the funnel: presenting & prioritizing candidates, vs. recommending or sizing investment terms. A model that is a tool to wield vs. a competitor to your job. [TODO PHRASING] -->

In the diligence phase, data leaders may also be valuable in informing how much upside a company might have available from making investments in data initiatives. However, this is a small piece of the puzzle in informing an investment, and therefore unlikely to be a big piece of the job.

### 2 Fractional Operator
Operating partners and other forms of fractional C_O often have key roles at VC & PE firms. For a data person, this may be a fractional or turnaround CDO, CTO, or CPO, who works with the firms' portfolio companies on an as-needed basis. 

At PE firms, known for cutting costs, fractional leaders are often replacements for ousted execs; even so, [research](https://uncipc.org/wp-content/uploads/2022/02/IPC-Performance-Attribution-Analysis-v2022-02-12.pdf) shows that revenue growth is a top driver of value creation, and technology often plays a huge role in driving top-line revenue, especially when the acquired company is small and/or built on aging infrastructure, as many are. In such cases, I've seen experienced leaders deployed to just one major company, spending a year or more deep in the weeds, turning around an entire technology function. 

I've also spoken, however, with individuals employed by VCs who work with more than 10 portcos at a time. a16z is largely credited with establishing this founder-supporting strategy, "[helping great entrepreneurs build great companies](https://www.businesswire.com/news/home/20120131005976/en/Andreessen-Horowitz-Announces-1.5-Billion-Fund-III)" by providing access to operator resources as-needed.

### 3 Platformization
Data teams are often leveraged to drive efficiencies via platform development. Many firms specialize their investments in certain industries or sectors, and thus portfolio companies can end up facing similar problems and having similar technical needs [[4]](#4). Much the way corporate M&A can lead to rationalizing of services & systems, companies acquired by PE firms or with certain VC investors may find the relationship an opportunity to build less in-house, and instead buy or borrow centrally-developed platform elements. 

This setup can pair well with the fractional operator role: much like inside a large enterprise, where some part of the data team works on central platform components as others embed in specific areas of the business, VC/PE data operators parachuting in and out of portcos learn which data products would be most valuable to centralize. 

## Non-data roles for data people
### Angel investing
Angel investing allows anyone with access to deals to put up capital, just not on behalf of any LPs. Through [InvestInData](https://www.investindata.ai/), I've [seen](../a_year_with_investindata/) that data people can make great investors; I've also observed that our partners from Notable Capital come with a wealth of expertise that none of us fully possess. 

### Scouting
Network is key to the VC industry: access to deal flow is what determines the size of the top of the funnel, and the quality of companies entering it. Scouts develop mutually beneficial relationships with VCs, where the firm gets access to more (and hopefully better) deals, while the scout gets some financial upside and experience working with the VC. Due to my data experience, I've been approached by firms focused on companies who build data/AI infra, and have friends scouting for firms focused on ML/AI products.

### Should more data people found their own funds?
What can I say, it's on my mind.


# Feedback
I've spent spent a lot of time (years) knocking these ideas around with friends in the industry, but always love feedback. [Get in touch.](mailto:emilypastewka@gmail.com)

---


#### [1]
Especially true for PE firms. VC firms tend to be closer to tech, so they've experimented for longer with in-house data expertise. The [Private Equity Technology Podcast](https://podcasts.apple.com/us/podcast/private-equity-technology-podcast/id1265864756), which launched in 2017 but really started to get into data in 2019, covers a lot of PE tech strategies.

#### [2]
I partially didn't go into PE because I wasn't ready to leave startups, and partially because, well...[Brendan Ballou's book Plunder](https://www.amazon.com/Plunder-Private-Equitys-Pillage-America/dp/1541702107) says it better than I could (though I recommend reading it [non-linearly](https://notes.andymatuschak.org/zGyuqjqaSGWzT9ndJJVxiaw), as it's quite a depressing read). There are of course firms that specifically aim to do good along with doing well, but in the years that I considered these roles, those weren't the firms that had the money to hire me. 

#### [3]
Rebel Fund identifies as a very data-driven fund, and describes their model in a [blog post](https://jaredheyman.medium.com/on-rebel-theorem-3-0-d33f5a5dad72). The majority of its features, and those that are top-ranked, are founder-based. They even state, "[company attributes] don’t matter nearly as much as the founders themselves." The author shows in the post that the model's investment decision backtests well, but doesn't show a comparison to what they did or would have invested in without the model. It's also worth noting that this firm only invests in YC companies, which already [outperform, on average](https://jaredheyman.medium.com/on-the-176-annual-return-of-a-yc-startup-index-cf4ba8ebef19). 

#### [4]
[Imaginary Ventures](https://www.imaginary.co/), for example, describe themselves as "a leading venture capital firm investing in the most generationally-defining consumer businesses." Interestingly, they chose to invest in the platform play via another portco rather than develop for it internally: in 2021, they led Black Crow AI's $25M seed round. Many of their core DTC portfolio companies became Black Crow customers. A hybrid model I've seen is the incubation path, where a lean team building a platform tool is set up in such a way that, if successful enough, the investor will spin them out into their own startup; if not, they are maintained centrally or absorbed by a single large portco.
