<!--
.. date: 2024-03-17
.. tags: cleantech
-->

# Web3: 3D printing at worst, solar at best

_One day live and I already have some interesting notes & counterarguments in my inbox/DMs. Safe to say this post is going to feel dated pretty fast._

When I got this site up last month I [expected](https://emilywbailey.github.io/posts/why-now/) my first series of posts to describe my journey through data science and tech leadership. These would be helpful resources to have on hand following several conferences, panels, and meetings with student groups I’ll be joining over the next few months, but the truth is I am way too interested in the world right now to start by writing about myself.

I find writing a highly effective method of processing information and, like much of the world, have been spending a fair amount of mental energy lately trying to elucidate a coherent thesis on web3 [[1]](#1). Scribbled iPhone Notes have only gotten me so far; this is my attempt to further marshal my thoughts.

Crypto as a concept isn’t new to me. I had very early friends at Coinbase, my fiancé’s company went through a [Bitcoin-focused accelerator](https://www.boost.vc/about-us) back in 2013, and working in tech during the bitcoin surge of 2017 generally meant a constant [deluge](https://twitter.com/lbudorick/status/971849467539341312) of LinkedIn messages from founder-recruiters in the space.

I was interested, but I loved what I was doing in the data world, and Uber was a great place to learn and build those skills. I also didn’t love the escalating energy intensity required to mine crypto & how it was being generated. Given the risks we understand about global climate change and the way I’ve dedicated my time to this space, the potential upside of distributed financial technology just wasn’t enough for me.

However, the space is quickly evolving. Mining ETH2 via [proof of stake](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/) instead of proof of work is bringing energy expenses down dramatically. Arguments abound that this will [destabilize](https://twitter.com/JasonPLowery/status/1495528915485564932) the nascent system, but whether this is where we land or not, it shows an alternate path forward, and willingness of the community to explore those alternatives. This renewed my curiosity — and whether this is the primary reason most people have become crypto-enamored of late or if it’s simply for the promise of riches, the overwhelming interest in the space does make learning fun. Smart people are sharing nuanced views on podcasts and Twitter. My friends are taking blockchain data courses and joining covens. I’m no longer limited to screaming over bad karaoke in a dark bar full of early HODLer bros to learn about this space.

If you’ve ever done an Insights Discovery analysis, I’m blue-dominant: I like to gather a lot of data before making decisions. I’m also constantly thinking about the Dunning-Kruger effect and wondering how far right on the x axis I really am in a given space. When it comes to crypto, I’m pretty far to the left. I haven’t built a dApp or joined a DAO. I’ve only traded the 2 most common currencies. I still stumble when older relatives ask questions that go too far beyond the surface on mining and minting. But I’ve got a working hypothesis that helps me think about where things might be headed, some reasonably cogent arguments to back it up, and a proposal for the data to seek over the next few years. I’m skeptical of my own thoughts, but that’s why I’m writing them down. I look forward to coming back to this in future months and years to reevaluate and learn.

**First things first: how do we define success for web3?**

I coach my team to ask this question before digging into any data: what is the goal? Before trying to understand where web3 might be headed, it’s important to understand where it’s trying to go.

This answer seems to differ quite radically for different people [[2]](#2). Is it about [transparency](https://www.wired.com/story/web3-gavin-wood-interview/) in tech? In government? In banking? Is it about empowering creators? [Overthrowing oppressors](https://twitter.com/kelseyhightower/status/1495822054817415168)? Is it just about making a ton of money?

Web3 companies abound aiming to address all of the above, so I’m going to choose a proxy metric: success of web3 means success of many companies relying on blockchain technology to meaningfully disrupt how we go about our lives today.

I will continue to remind you, this is an early foray into my thoughts, so this may be an objectionable abstraction. Fair criticism. But let’s see what we learn by following this success metric across a few other industries and bringing the learnings back to web3.

**Thesis: Web3 is 3D Printing at worst, solar at best**

3D printing was introduced to the world in the 1980s (I know, right?), but today’s conversations about this field really [started in 2011-12, with a peak in interest around 2015](https://trends.google.com/trends/explore?date=all&geo=US&q=3d%20printing). Gartner [nailed](https://www.gartner.com/en/newsroom/press-releases/2015-08-18-gartners-2015-hype-cycle-for-emerging-technologies-identifies-the-computing-innovations-that-organizations-should-monitor) that prediction. They have NFTs around the same point on [this year’s chart](https://www.gartner.com/en/newsroom/press-releases/2021-08-23-gartner-identifies-key-emerging-technologies-spurring-innovation-through-trust-growth-and-change).

So what happened to 3D printing? It found a niche — well, a few. Medical technology and manufacturing prototyping have become [well-proven areas of impact](https://www.3dnatives.com/en/wp-content/uploads/sites/2/gartnerreport.jpg) for this technology. Efforts remain in other spaces, but there are gaps to the promise of the early twenty-teens: [equipment, materials, knowledge](https://redshift.autodesk.com/5-problems-with-3d-printing-and-how-to-fix-them/).

Compare this to web3. Are there gaps in equipment? Well, we don’t all have a server to run our own blockchain, as Moxie Marlinspike so clearly points out in his well-read [essay](https://moxie.org/2022/01/07/web3-first-impressions.html). Sure, this is a personal choice, but is it likely to change? I tend to agree with him: I think not. Modern-day engineers like to build fast, and that means being willing to stand on the shoulders of giants. One need only look at how web2 turned out to see that. Materials? Unlike bitcoin, Ethereum is unlimited, but in practice, most people are priced out of owning a meaningful amount. Knowledge: this is perhaps the easiest gap to close. Web3 is exciting to people, the activity around learning and building in this space is buzzing. The last time my Twitter feed shifted this abruptly was during the 2016 presidential election cycle.

So it seems equipment is the biggest sticking point. Moxie lands here as well, and to summarize some of his learnings: the community is already consolidating around platforms that solve the equipment problem. Big players like Etherscan, Infura, OpenSea, Coinbase are layers between the blockchain and client applications that allow developers access to the data without direct interaction. This...isn’t decentralization!

I had a conversation recently with a friend who’s been in the space for a while, and he pointed out that web3 centralization isn’t so bad, because unlike web2 these players don’t own the data, they just provide access to it.

This feels partly true. Meta, for instance, owns the information on your Facebook likes, your Instagram posts, your Whatsapp connections. It feels less likely that a web3 company could build nearly as much value in the same way — after all, transactions are on the blockchain. But it’s not impossible. There is plenty that could take place off the blockchain on these platforms that is easily monetized. As consumers, we either need to be vigilant about using platforms that don’t collect anything except what we’re explicitly contributing to the open ledger, or accept that we’re not guaranteed to end up so far off from where we started on web2.

However, I don’t fully agree. The value of data doesn’t just come from owning it, but also having the means to take advantage of it. One need only check out a Kaggle competition to see this truth. Even better, remember the [Netflix Prize](https://web.archive.org/web/20090924184639/http://www.netflixprize.com/community/viewtopic.php?id=1537)? A group of researchers won one million dollars for creating the best user-film rating algorithm using Netflix data. It outperformed Netflix’s internal best effort by more than 10%! It was 2009 — Netflix then certainly didn’t have the same resources as Netflix of today — but that’s the point. Compute power & knowledge of how to use data go far. These companies are explicitly building those systems and teams.

I’m not (by a long shot) the first to say that web3 could be as centralized as web2. And, as I mentioned earlier, I’m not nearly educated enough in this space. But from where I sit, this feels like a big problem for the promises being discussed. Here’s where we get back to 3D printing: to me, true decentralization feels unlikely to succeed (at least soon — I’ll get there in the next section). Some applications of a distributed ecosystem, however, feel really viable: the value of application to spaces like online ticket sales and digital art, for instance, may really outweigh the costs I described above. Like manufacturing and healthcare in 3D printing, these may be two of just a few use cases that stabilize for the long term.

So, I don’t know, is this success? Congratulations, you win a new acronym to complain about that isn’t FAANG. I’d say that’s not really what we meant.

**But...maybe web3 is more like Solar.**

Solar energy is as old as time, there’s really no other way to say it. Humans have been harnessing the sun in various ways for as long as we’ve been on this planet. In the late aughts [[3]](#3) the idea of solar power reducing our reliance on fossil fuels was [on a tear](https://trends.google.com/trends/explore?date=all&geo=US&q=solar%20power). By 2013, it had entered the Gartner [trough of disillusionment](https://cdn2.hubspot.net/hub/48858/file-14362507-png/images/fig1-gartner-hype-cycle-arteris-noc-20121-resized-600.png). By 2014 it was sliding up the [slope of enlightenment](https://www.gartner.com/en/newsroom/press-releases/2014-12-15-gartner-says-india-green-it-and-sustainability-spending-to-reach--34-billion-in-2014), but the Trump years put a kibosh on meaningful progress in the energy space and it fell off the map entirely.

Except, it didn’t. Let’s go back to equipment, materials, knowledge, but do them in reverse this time. Knowledge: humans have been studying electricity for hundreds of years. As an end user, it’s pretty straightforward to put some panels on your roof and hook an energy generator up to a grid. Materials? The sun shines more consistently in some places, so this is more of a mixed bag. Equipment is once again the kicker. Solar panels got really good and cheap over the time frame we discussed, but it took batteries a long time to catch up to any meaningful degree. Tesla has of course had a huge impact on driving (ha-ha) this space forward, which has in turn lessened the ‘materials’ concern as well (the better you can store power, the fewer hours of solar output you need).

So here we are, 2022, well beyond the time we all hoped to see solar, but it is finally happening at a very real scale. A leader I know in the field told me recently she has not felt this energized (I crack myself up) about the space in her entire career. Could we see a similar post-trough global renaissance with web3? What would this look like?

A few years from now, web3 might not be in the news so much. We’d enter the trough of disillusionment (this may not be far away). But engineers love hard problems, and the web3 community is strong. Usage of social media has matured far beyond where it was when 3D printing and solar were hot, and DAOs are introducing new structures of tying financial outcomes to innovation by groups. Could we see breakthroughs in energy efficiency or client-side blockchain driven by groups outside of venture-funded firms?

This, to me, doesn’t feel entirely unlikely. There may not be any political movements stomping all over crypto in the same way as the Trump years did solar. This could mean creative solution generation to the web3 equipment problem occurs at a much more rapid pace [[4]](#4). In addition, web3 is not your typical gold rush. The inequality in ownership of crypto assets is enormous [[5]](#5), which means crypto-wealthy individuals hyping the technology will be the ones who win the biggest: it’s a serious motivation to keep pushing forward no matter the legitimacy of the hype. [[6]](#6) I won’t go as far as to say [“it’s a ponzi,”](https://www.theatlantic.com/technology/archive/2022/02/crypto-nft-web3-internet-future/621479/) that feels like condemning all of VC, but especially with the ability to stake currencies, the shape of the system sure does appear to be a pyramid. [[7]](#7)

I can make related arguments, however, for why a golden age of web3 will never come.

Hot take alert: I’m not optimistic about political stability anywhere on this planet. [[8]](#8) Some political changes could accelerate innovation, yes, but changes that lead to swifter and firmer regulations on crypto (hot take alert 2: I don’t hate this) would reduce confidence in its viability, pushing a lot of aspiring wealth-builders into different fields. The inequality of ownership will have the same impact, should a downturn go too low too long: nobody besides the whales will be financially incentivized to Hold On for Dear Life. MetaMask founder Dan Finlay [says](https://medium.com/@danfinlay/what-moxie-missed-on-web3-wallets-8dc572e7f39b) “web3...springs from a patchwork of deep wounds from a lifetime of being betrayed by seemingly every centralized institution that ever gained our trust.” If the cracks in web3 go too long unpatched, this community may easily turn their backs on yet another system that has failed them.

**Ok, so basically, it will work or...it won’t. Nice one Emily.**

Like I said, I like to gather a lot of data before I have strong confidence in a position. But give me a little credit, I do think I narrowed down a few specific hypotheses here:

- Web3 doesn’t have no promise

- It’s just very unlikely to be as big as it sounds within the next decade

- Specific use cases will likely mature soon

- And the big shift, if it comes, will be dependent on some key innovations in “equipment”

These may not be so different from the global consensus, and that’s ok. That was never my intention. I aim to understand my own perspective, and this act of writing has helped me to clarify that.

Over the next few years, I’ll be tracking my proxy metric closely, i.e. watching web3 startups to see how many gain real traction, and whether this occurs primarily in specific industries. I’ll be continuing to track inequality in cryptoland. And I’ll be keeping a pulse on my conversations with friends & colleagues (and yes, ok, Twitter) to understand what ideas & fears are rising to the top among intelligent people who know more than I do about the space.

**What else do I need to say?**

In case I haven’t said this enough, I still have so much to learn about this space. In particular, as a data person, I’m ashamed to say I have yet to get my hands dirty with any blockchain data. I’m itching to do so, but in the middle of a few too many things right now and a bit of a stickler about my sleep. It’s on the list! Expect a follow up when I get there.

Also, I don’t have comments set up here, so you are cordially invited to [tweet at me](https://twitter.com/emilywbailey/status/1498506320575610882) pointing out so the gaping holes in my knowledge.

---


*Thank you David for many conversations with me about these topics. Never bored with you and your giant brain. Thank you also Brad for the debates and Amit for offering to read this draft.*


---


#### [1] 
it is important to note that I don’t mean [semantic web](https://en.wikipedia.org/wiki/Semantic_Web) but rather the [blockchain based decentralization of the web](https://en.wikipedia.org/wiki/Web3)

#### [2]
[web3 is the mirror of Erised](https://blockworks.co/why-all-the-hate-directed-at-web3/) it all makes sense now.

#### [3] 
this term also feels like a recent trend... [semi](https://trends.google.com/trends/explore?date=all&geo=US&q=aughts)-[confirmed](https://trends.google.com/trends/explore?date=all&geo=US&q=early%20aughts)

#### [4]
Vitalik Butarin sure [thinks so](https://www.reddit.com/r/ethereum/comments/ryk3it/my_first_impressions_of_web3/hrrz15r/) and he is better informed than I am so

#### [5]
2022-03-01 edit: I originally had [this paper](https://www.nber.org/system/files/working_papers/w29396/w29396.pdf) and [this WSJ article](https://www.wsj.com/articles/bitcoins-one-percent-controls-lions-share-of-the-cryptocurrencys-wealth-11639996204) cited here but they both only discuss bitcoin. *big miss*

#### [6]
how can one write a post on web3 without including [this gem](https://twitter.com/jack/status/1473165759224463360?lang=en)

#### [7]
maybe that’s all of modern capitalism and not a bug unique to crypto...pretty stable so far, guess that backs up this case

#### [8]
I wrote this sentence Feb 21st, AKA before Feb 24th. *yikes*