+++
title = "The Year in Ethereum 2018"
date = 2019-01-16T00:00:00
description = ""
tags = ["ethereum", "year-in-review"]
draft = false

[params.cover]
image = "cover.png"
alt = "The Year in Ethereum 2018"
caption = "The Year in Ethereum 2018"

+++

*By Josh Stark & Evan Van Ness*

**Ethereum began as a bold experiment.** Can we build a universal platform for digital money and assets, un-censorable applications, and decentralized organizations?

We started with a slightly smaller experiment: was it possible to launch a blockchain that could execute arbitrary programs? Over time, the Ethereum community began new experiments. Would developers find it interesting? What applications are actually useful? The community learned from its successes and failures, and iterated on their work. New people joined the community and started running their own experiments.

In 2018, the Ethereum community ran more experiments than ever before. What did we learn? This summary of the year in Ethereum is our attempt to identify the most important developments — the things that we'll say mattered, 10 years out.

These developments took place at every level of the Ethereum "stack". This includes the core protocol and the clients that implement it, commonly referred to as "Layer 1". It includes the supporting developer tools & infrastructure, that make engineering on Ethereum possible. It includes "off chain" technologies, that let developers build fast and performant applications. And it includes the products and businesses built on Ethereum.

Keeping track of everything in this ecosystem is becoming more and more difficult every week. There are competing implementations of many infrastructure technologies — including two clients with ~50% ([Geth](https://github.com/ethereum/go-ethereum)) and ~40% ([Parity](https://www.parity.io/ethereum/)) of the network. There are multiple competing off-chain technology stacks being built, multiple ETH 2.0 clients under development, and most markets have multiple competing businesses. It feels messy and chaotic — the Ethereum ecosystem is [a bazaar, not a cathedral](http://www.catb.org/~esr/writings/cathedral-bazaar/cathedral-bazaar/). While this can make it hard to follow, it's a credit to the community: we're too big to measure with simple tools.

Our goal is to help you sort through that noise and see the bigger picture. In our view, here are the most important developments in 2018:

* **1. More people started using Ethereum**, for more things — but we're still far from mass adoption.
* **2. Decentralized Finance (DeFi) and stablecoins** — a new class of applications that saw many product launches and some breakout successes.
* **3. The year of #BUIDL** — it became radically easier to build applications on Ethereum. Our development and security tooling improved significantly, we got better at sharing best practices, and hackathons became a trend.
* **4. Layer 2 scaling** — multiple "layer 2" applications launched, and we made critical progress towards making these scaling solutions easy to use for developers.
* **5. Zero knowledge technology** — this year it felt like every technical conversation in Ethereum was "We can do it this way right now, but of course once we have good zkSTARKs…"
* **6. ETH 2.0 / Serenity** — the roadmap solidified, and it moved from a research project to an engineering effort.

![divider](divider.png)

## 1. Did adoption of Ethereum grow in 2018?

From 2015–2017, it was an open question whether there would ever be any demand for Ethereum. Today, that answer feels settled: since late 2017, the Ethereum blockchain has continued to be used near maximum capacity:

![Ethereum gas utilization showing near-100% capacity usage](ethereum-gas-utilization.png)

Source: Google Bigquery Ethereum public dataset

This graph shows the utilization of the Ethereum blockchain at different points in time. Specifically, [it is a measure of the total gas used divided by the gas limit](https://twitter.com/nicksdjohnson/status/1084382703951130624). When the line approaches 1, it means the Ethereum blockchain is being used at nearly 100% capacity.

Yes, the graph above is encouraging — people are paying to use the Ethereum blockchain. But it means we started asking harder questions: we're near 100% capacity even with such a small user base? What would happen to fees if we on-boarded millions of users, when the total capacity of the network is so low? How many people actually use Ethereum? What are they using it for? And what are the right metrics to measure growth?

Measuring "use" of Ethereum isn't easy. For instance, we can get a basic picture using raw on-chain statistics, like the [number of transactions on the network](https://etherscan.io/chart/tx):

But this doesn't tell the whole story. If Ethereum was being used near full capacity, how can the number of transactions be declining? The composition of transactions on Ethereum shifted from a large number of simple ones, to a smaller number of complex ones. For instance, token transfers (~50K gas) or opening up a MakerDAO CDP (up to 900K gas) both "take up" more of the network's capacity than a simple ETH transfer (21K gas).

As Ethereum's app layer continues to grow, we should expect the transaction count to decline while the chain operates at full capacity. And as more activity moves into side chains, state channels, or plasma chains (see Layer 2, below), measuring on-chain transactions increasingly only tell part of the story.

### What are people using the network for?

Many significant and long-awaited applications went live in 2018, and appear to be attracting users.

[Dai](https://makerdao.com/dai/), the stablecoin launched by [MakerDAO](https://makerdao.com/), has been live since late 2017, and the total supply of Dai grew to 69m as of December 31st, 2018.

![Dai supply growth over 2018](dai-supply-growth.png)

Source: mkr.tools

Users of MakerDAO have locked more than 1.7% of all ether into smart-contracts that serve as collateral for the Dai stablecoin. As of December 31st, the value of that ether was over $275 million. We discuss MakerDAO, and other "decentralized finance" applications, in detail in the next section.

[Augur](https://www.augur.net/), a decentralized prediction market under development since 2015, launched in July 2018 and has seen open interest (the amount of value currently "bet" on the system) grow to a high over over $2.96m in November 2018. However, the total number of users has remained low.

[Spankchain](https://spankchain.com/), a payment channels service for the adult entertainment industry, launched in April 2018 and [processed $70,000 in payments](https://www.coindesk.com/spankchain-eth-crypto-porn-camgirl) to performers between April and December 2018.

Many more applications launched in 2018, including many in the "decentralized finance" category. Many others were games like [Gods Unchained](https://www.coindesk.com/a-crypto-card-game-is-testing-magics-records-and-it-hasnt-even-launched) (beta, November 2018), or gambling services like [FunFair](https://funfair.io/) (mainnet, September 2018). There are hundreds of other applications that use the Ethereum blockchain, which you can find listed [here](https://www.stateofthedapps.com/rankings/platform/ethereum) or [here](https://dappradar.com/dapps).

Overall, consumer use of applications on Ethereum remains low. When we use measurements like daily active users who interact with a dapp's smart-contract on the blockchain, we see an average of [between 10,000–15,000](https://dappradar.com/charts) users on any given day in 2018.

However, note that this is a measurement of on-chain transactions and does not include, for example, someone opening an app and browsing their collectibles, or opening [Veil](https://veil.market/) (alpha, September 2018, mainnet January 15 2019) to view their open predictions on Augur.

User adoption of new technology moves in phases. Users come to applications, creating demand for better infrastructure, and applications then build on that infrastructure to meet the expectations of users. We can analogize from web development that there is a reinforcing [loop of app and infrastructure development](https://www.usv.com/blog/the-myth-of-the-infrastructure-phase).

By the end of 2017, we had learned that there was demand from people who wanted to build applications on Ethereum. In 2018, the community shipped apps that were useful without scaling upgrades, and built infrastructure that will make it possible for the next wave of applications to work at a larger scale.

![divider](divider.png)

### What should we be measuring, anyways?

Is "daily active on-chain transactions" the right measurement to quantify user adoption? This year, people started thinking (and [tweeting](https://twitter.com/sassal0x/status/1058322555315019777)) about what metrics we should use to gauge Ethereum's success.

The answer, surely, is that it depends on what counts as success. Some businesses require large numbers of users (like consumer apps or games), while others seek high volumes of value (like some financial services).

As layer 2 scaling technologies are adopted, more user activity will move "off-chain" where it is more difficult to measure. This already influences the data used to measure Ethereum's adoption. For instance, [DappRadar](https://dappradar.com/) does not currently include statistics on games that use [Loom](https://loomx.io/)'s Dappchains, nor does it list activity in [Spankchain](https://spankchain.com/)'s payment channels.

But this isn't a bug, it's a feature. We want to build [web 3](https://medium.com/l4-media/making-sense-of-web-3-c1a9e74dcae) — an internet that, among other things, respects user's privacy instead of spying on them. That means giving users the option to keep their business to themselves, off-chain, where it isn't easy to measure and incorporate into statistics.

![divider](divider.png)

## 2. The Year of DeFi

This year we talked about a new narrative within the larger set of Ethereum applications. Many projects launched which were explicitly financial — applications or protocols that give users new tools with which to manage and use Ethereum-based money or assets. As a group, these became known as "Decentralized Finance" or "[DeFi](https://medium.com/defi-network/opening-defi-42a5afdb71e0)".

There are now companies building out a stack of financial primitives — the basic building blocks of a financial system. While these tools are in very early stages, it is possible today to use Ethereum-based protocols to take out loans, to lend money and earn a return, to buy bundles of assets, to hedge your risk, to trade assets trustlessly, and to make payments for zero fees. Because these systems are largely open and interoperable, it is becoming possible to combine them in useful ways, building applications that can borrow, lend, and invest simply by calling an API.

Within this category there are stablecoins ([Dai](https://makerdao.com/), mainnet December 2017), lending tools ([Dharma](https://blog.dharma.io/dharma-community-update-29-may-2018-3fe21f3c93c6), mainnet May 2018, [Marble](https://marble.org/), mainnet beta July 2018), margin trading and derivatives products ([Daxia](https://www.daxia.us/), mainnet January 2018, [dYdX](https://dydx.exchange/), mainnet October 2018, [bZx](https://b0x.network/), mainnet September 2018, [Market Protocol](https://marketprotocol.io/), testnet November 2018, [UMA](https://medium.com/uma-project/uma-enabling-universal-market-access-266eb9e5fd90), under development), bundled investment products ([Set Protocol](https://www.setprotocol.com/)), and many others.

Over the last year, the share of ETH "locked up" (e.g. used as collateral) in the smart-contracts of some DeFi applications has grown:

![ETH locked in DeFi applications excluding MakerDAO](defi-eth-locked.png)

The above graph hides MakerDAO by default, in order to let us see other applications. If we include MakerDAO, the graph looks like this:

![ETH locked in DeFi applications including MakerDAO](defi-eth-locked-with-maker.png)

The most successful DeFi protocol — and the most successful application on Ethereum in 2018 — is [MakerDAO.](https://makerdao.com/)

Over the last year Dai survived a 94% fall in the value of its underlying collateral. The system was battle-tested in the first few months of its launch, and appears to have functioned as intended. It has quickly became a core piece of infrastructure for many Ethereum applications.

Within the community of people that actually use Ethereum apps on a regular basis, it's hard to overstate the impact of having an easy to use, decentralized stablecoin. If you work in this ecosystem, you will remember that 12 months ago you probably sometimes paid, and were paid, in ETH. Today, everyone uses Dai — for contract payments, for event sponsorships, for petty cash.

MakerDAO is not just Dai, though that is the most outward-facing product. It also includes a system of "[Collateralized Debt Positions](https://cdp.makerdao.com/)" (CDPs), which allows anyone to lock up ETH as collateral and receive a "loan" in DAI. This system facilitates the collateral backing that makes Dai possible, while also being a lending product in its own right that can be used for, among other things, leveraged trading.

Dai is not the only stablecoin built on Ethereum — though it is the only one of significant size that is "decentralized" in the sense that it is backed by digital assets in an automated collateral system, rather than off-chain assets like dollars held in fiat bank accounts. Other Ethereum-based stablecoins include [TrueUSD](https://www.trusttoken.com/trueusd/) (mainnet March 2018), [Paxos](https://www.paxos.com/) (mainnet October 2018), [Gemini Dollar](https://gemini.com/dollar/) (mainnet October 2018), [USD Coin](https://www.coinbase.com/usdc) (mainnet October 2018), and [sUSD](https://www.synthetix.io/) (mainnet June 2018).

Collectively, all stablecoins built on Ethereum had a [marketcap of ~770 million](https://stablecoinindex.com/marketcap) at the end of the year, large enough that as a group they would have ranked as the [14th largest](https://coinmarketcap.com/historical/20181230/) cryptocurrency on Dec 31.

While significant and growing, this volume is still dwarfed by trading volume in [Tether](https://tether.to/), which during the same period saw a daily average of around $5 billion USD.

Within the broader category of DeFi, decentralized exchanges (DEXs) are the next most significant. In 2018, this ecosystem grew and matured. There are not just multiple competing DEXs, but multiple types of DEXs now live in production. However, volume [remains low](https://dex.watch/) compared to any centralized exchange.

There are now several DEXs that use the [0x protocol](https://0x.org/). [Radar Relay](https://radarrelay.com/) launched their beta in August 2017, raised a series A in July 2018, and released v2 of their product a few months ago in September. [Paradex](https://paradex.io/) launched October 2017, and was [acquired by Coinbase](https://blog.coinbase.com/welcome-paradex-to-coinbase-62f16cc9bd74) in May 2018. [DDEX](https://ddex.io/) launched their open beta on January 9 2018, became the leading 0x relayer by volume, and recently announced that they are forking the 0x protocol to create [a competing protocol called Hydro](https://hydroprotocol.io/).

This year saw an expansion of the type of DEXs built on Ethereum. [Kyber](http://kyber.network/), which launched in March 2018, does away with the order book and simply lets users receive a quote, and instantly swap one asset for another. [Airswap](https://www.airswap.io/), which launched in April 2018, similarly provides a simple "token swap" service.

[Uniswap](https://uniswap.io/), which implements a novel automated market-making feature [inspired by a reddit post from a few years back](https://www.reddit.com/r/ethereum/comments/55m04x/lets_run_onchain_decentralized_exchanges_the_way/), launched in November 2018. It operates entirely on-chain, and [makes markets itself using a deterministic algorithm](https://medium.com/@cyrus.younessi/uniswap-a-unique-exchange-f4ef44f807bf). Gnosis' DutchX protocol went live on mainnet in [October 2018](https://blog.gnosis.pm/the-dutchx-pilot-d8f41daf64f7).

Why did DeFi take off in 2018? One reason is that many of these applications are useful today, even before critical scaling technologies are in place. Basic financial use-cases like lending and borrowing do not require high transaction throughput — they simply require a secure programmable base layer blockchain. Ethereum's simplest use-case is the creation, exchange, and use of digital assets like ETH. One way of looking at DeFi is that it is simply building the basic financial infrastructure to use those digital assets.

![divider](divider.png)

## 3. The year of BUIDL — better tools, better frameworks, more hacking

2018 was the year of #BUIDLing. This was the year that it became radically easier to get started building applications on Ethereum.

Developer tools improved, new security tools were released, key frameworks were released, and hackathons became a fixture in the community. In 2018, the vision of average developers being able to build something useful on Ethereum became a reality, and the tooling necessary to use smart contracts in production improved.

We even gained a new meme to go along with the technical progress: BUIDL. While the term — an inversion of the bitcoin meme "[HODL](https://twitter.com/coindesk/status/1083567269953839104)" — had been used by [different people](https://twitter.com/balajis/status/1070830466989678592) over the years, it never gained any real traction until [ETHDenver](https://ethdenver.com/) in February 2018. In the weeks following, it became an unofficial mantra for the Ethereum community — a reaction against the unhealthy focus on price and speculation common across the crypto industry.

![divider](divider.png)

### Security tooling

At the end of 2017, security tooling & best practices were on everyone's mind. Multiple high profile hacks and [security failures](https://medium.com/cybermiles/i-accidentally-killed-it-and-evaporated-300-million-6b975dc1f76b) forced the Ethereum community to improve best practices, and invest more resources in security audits and tooling.

In 2018, the Ethereum security community improved. New security tools became available that made it easier to build secure applications. [Trail of Bits](https://www.trailofbits.com/) [released several tools](https://blog.trailofbits.com/2018/03/23/use-our-suite-of-ethereum-security-tools/) in March 2018 (who also maintain a useful list of resources [here](https://github.com/trailofbits/awesome-ethereum-security)), including static analysis tools, fuzzing tools, and more. [Securify](https://securify.chainsecurity.com/), an automated security scanner for Ethereum smart contracts, was [released in July 2018](https://medium.com/chainsecurity/researchers-release-a-free-state-of-the-art-security-scanner-for-ethereum-smart-contracts-b58b57ce0e38). Mythril, a security analysis tool initially released in 2017, became a platform and re-branded to [MythX](https://twitter.com/mythx_platform).

The Ethereum security community made progress towards "best practices", though the community doesn't always agree on all of them. Valuable resources like the [Smart Contract Weakness registry](https://smartcontractsecurity.github.io/SWC-registry/) helped the industry share best practices and common anti-patterns. Notable "traditional" security researchers began working in the Ethereum space, including [Trail of Bits](https://www.trailofbits.com/) and [Sigma Prime](https://sigmaprime.io/), adding to the stable of high-quality auditing firms already working in the space.

Despite this progress, there's still significant work required. In particular [better formal verification frameworks and tooling](https://media.consensys.net/how-formal-verification-can-ensure-flawless-smart-contracts-cbda8ad99bd1), which is a consistent complaint from developers building on Ethereum.

![divider](divider.png)

### Infrastructure

Ethereum's primary clients — [Geth](https://github.com/ethereum/go-ethereum) and [Parity](https://github.com/paritytech/parity-ethereum) — continued to be improved and refined, thanks to essential work by their development teams. New clients were released, like [Pantheon](https://github.com/PegaSysEng/pantheon) in Java and [Nethermind](http://nethermind.io/) in .NET Core.

There has long been an understanding that Ethereum needs to diversify the node infrastructure available to application developers. This market has long been dominated by [Infura](https://infura.io/), but in 2018 [many teams began working on alternatives](https://www.coindesk.com/the-race-is-on-to-replace-ethereums-most-centralized-layer).

[Dappnode](https://dappnode.io/), a project to make it cheap & easy to run a personal Ethereum node, [launched in July](https://medium.com/@DAppNode/dappnode-the-infrastructure-for-the-decentralized-world-85983b16db14) (you can even [buy a pre-configured one](https://ava.do/)). [VIP node](https://vipnode.org/), a service that allows users to "subscribe" to node access thereby creating an incentive for more full nodes, [went live this year](https://medium.com/vipnode/an-economic-incentive-for-running-ethereum-full-nodes-ecc0c9ebe22). [Denode](https://github.com/ChainSafeSystems/denode), a project that similarly seeks to provide market incentives for more decentralized node infrastructure, received a grant from the Ethereum Foundation in September. Other projects — like [LightJS](https://github.com/paritytech/js-libs) by Parity, [released in November](https://www.parity.io/light-js-how-to-build-your-dapp-on-a-light-client/) — make it easier for developers to build dapps that don't need to rely on full nodes.

Decentralized storage solutions like [IPFS](https://blog.ipfs.io/) and [Swarm](https://blog.ethereum.org/2018/06/21/announcing-swarm-proof-of-concept-release-3/) continued to make progress. Swarm POC3 was [released in June](https://blog.ethereum.org/2018/06/21/announcing-swarm-proof-of-concept-release-3/), and now includes a messaging layer. The [Ethereum Name Service](https://ens.domains/) (ENS), a decentralized service that lets people use human-readable names (like alice.eth) in place of Ethereum addresses, [launched a mainnet integration](https://easydns.com/blog/2018/09/02/ethereum-name-service-ens-integration-now-live-on-mainnet/) with the .xyz domain registry (September 2018), and [announced](https://medium.com/the-ethereum-name-service/luxe-launch-looms-a70c950ffd43) a planned integration with .luxe.

![divider](divider.png)

### Developer collaboration across the ecosystem improved

The global community of Ethereum researchers & developers got better at working with each other in 2018. The primary forum for cryptoeconomic research on Ethereum — [ethresear.ch](https://ethresear.ch/) — only launched in August 2017, and was not widely used until early 2018. Today it is the de-facto R&D hub for Ethereum, and an essential technical resource for everything from plasma to sharding.

The very first Plasma researcher's call didn't happen until [January 2018](https://www.youtube.com/watch?v=_DPftmg7zR8), and the first state [channels researcher calls](https://www.youtube.com/watch?v=czb9Zh8P1y4) weren't until August 2018. There are now many [public calls](https://docs.google.com/spreadsheets/d/1Wg_eX-mYopvWT3LeHe4-FEHOtJoG28h8YcHl4PFTX5k/edit#gid=0) related to Ethereum development, ranging from core development of the protocol, to layer 2 tech, to individual areas like curation markets or product management.

The [ETHSecurity community](https://medium.com/coinmonks/learnings-from-the-ethsecurity-community-57431ae0ed5e) formed in mid 2018 to try and share best practices and shared learnings. The [fellowship of Ethereum magicians](https://ethereum-magicians.org/) — a community of Ethereum developers aimed at producing better EIPs and improving Ethereum's technical maintenance — launched in early 2018.

[Gitcoin](https://gitcoin.co/), a project that facilitates bounties for open-source development, launched their pilot in November 2017. In 2018, their platform was used to pay out ~$500,000 in bounties and grants to more than 700 developers.

![divider](divider.png)

### Hackathons became a big deal

In October 2017 [ETHWaterloo](http://ethwaterloo.com/) set a record as the largest Ethereum hackathon ever, which was quickly beaten by [ETHDenver](http://2018.ethdenver.com/) in February 2018. Over the rest of the year, there were 6 more [ETHGlobal](http://ethglobal.co/) hackathons that served more than 5,800 developers, as well as other events like [ETHMemphis](https://ethmemphis.com/) and two hackathons held by [Status](https://dev.status.im/).

In 2018 it was finally practical to run an Ethereum hackathon — there were enough developers who wanted to learn how to build on this tech, the ecosystem was varied enough that they had many interesting projects to work on, and the tools were mature enough that it was actually feasible to build a working demo in 36 hours. Many of the individual projects mentioned above — including the [Goerli testnet](https://www.ethnews.com/the-goerli-testnet-has-arrived), [Set protocol](https://www.setprotocol.com/), [Denode](https://github.com/ChainSafeSystems/denode), and [Cryptokitties](https://www.cryptokitties.co/) were conceived or launched at ETHGlobal events.

![divider](divider.png)

## 4. Layer 2: research, development, and live on mainnet

One of the early narratives about 2018 is that it would be [the year of Ethereum's layer 2 scalability solutions](https://medium.com/l4-media/making-sense-of-ethereums-layer-2-scaling-solutions-state-channels-plasma-and-truebit-22cb40dcc2f4).

The idea behind layer 2 scalability is to off-load computation from Ethereum onto "off chain" systems, while still retaining a blockchain's characteristic security guarantees. These off-chain systems can process transactions faster and more efficiently than the Ethereum main-chain, leading to more scalable payments or smart-contracts.

In 2017, there were no significant state channel or plasma chain projects live on mainnet, and few people understood the technology or its potential. What happened in 2018?

![divider](divider.png)

### State & Payment Channels

[State channels](https://www.jeffcoleman.ca/state-channels/) are the most basic layer 2 technique. At the start of 2018, there were several custom-built channels applications still under development. Today, many of those projects have launched to main-chain, and critical infrastructure has been built that will soon radically shorten the development cycle for channelized solutions.

[Spankchain](https://spankchain.com/) (micropayments through payment channels) launched their beta in April, and have been live in production ever since. [Funfair](https://funfair.io/) (casino games running in state channels) launched to mainnet in September. [Connext](https://connext.network/) (payment channel hubs for micropayments) launched their [first non-custodial hub on mainnet](https://medium.com/connext/our-first-hub-is-live-on-mainnet-b5660486635e) in September in collaboration with Spankchain. [Celer Network](https://celer.network/) (a state channel network & liquidity solution) launched their [testnet & demo apps in October](https://medium.com/celer-network/lighting-up-the-centauri-celer-network-sdk-and-testnet-launch-at-sfbw-7e257062b7af). [Raiden](http://raiden.network/), the long-anticipated ERC20 payment channel network, launched their [alpha release running live on mainnet](https://medium.com/raiden-network/red-eyes-mainnet-8c0f4ca05e5c) in December.

The number of live projects using channels will only increase as the technology becomes easier for developers to use. [Counterfactual](https://counterfactual.com/) (a framework that makes it easier to build a channelized application) published their work on generalized state channels in June, [open-sourced all their code](https://medium.com/statechannels/development-update-0-11-12-2018-b7002de5282e) in November, and is launching a full demo environment in January 2019. [Magmo](https://magmo.com/), a framework for a specific subset of channelizable applications ("[force move games](https://medium.com/magmo/an-overview-of-the-force-move-games-framework-for-state-channels-ff28f0962b07)") using state channels, [released a demo application at DevconIV](https://medium.com/magmo/we-launched-an-example-state-channel-app-17246bd98b05).

![divider](divider.png)

### Plasma

[Plasma](http://plasma.io/) is a scaling technique where operations are moved off-chain into a secondary blockchain, where they can be performed faster and at lower cost.

The idea is based on "sidechains", originally [a proposal to scale bitcoin dating back to 2014](https://www.blockstream.com/sidechains.pdf). Plasma introduced a novel improvement: unlike on a sidechain, a user of a Plasma chain would always have a guarantee that they can withdraw their assets to main-chain, even if the operator of that Plasma chain tried to censor or steal from them.

Plasma research has made large strides since the paper release in August 2017, though the technology remains further from production than state channels. The year began with only a few teams actively working on Plasma, as the research community began to explore various tradeoff and design choices within a family of related techniques derived from the original paper.

The majority of these designs have focused on the simplest use case: payments. These designs include Plasma MVP ([introduced by Vitalik in January 2018](https://ethresear.ch/t/minimal-viable-plasma/426)) and Plasma Cash ([introduced by Vitalik & Karl in March](https://ethresear.ch/t/plasma-cash-plasma-with-much-less-per-user-data-checking/1298), and the subject of [continuing formal work](https://github.com/loomnetwork/plasma-paper/blob/master/plasma_cash.pdf)). More recently, researchers have begun exploring zero-knowledge-proof based Plasma-like designs like the "Rollup" ([introduced by Barry Whitehat](https://github.com/barryWhiteHat/roll_up) in September).

Each of these can be augmented to mitigate their shortcomings, while minimizing tradeoffs. This unfortunately resulted in a "naming meme", where each new tweak on an existing design was given a unique name, leading to significant confusion for anyone not deeply involved in the research community. Useful taxonomies that divide up the design space are a work in progress.

At the same time, research continued into expanding Plasma beyond payments. While this work continues, current consensus among researchers is that an optimized "full EVM" plasma (which could run any smart contract) is a [complex challenge.](https://medium.com/@kelvinfichter/why-is-evm-on-plasma-hard-bf2d99c48df7)

This broad exploration of a large design space has been productive for researchers, but practical implementations are still mostly theoretical or in early stages. One exception is the Plasma Cash implementation built by Loom, [released in June 2018](https://medium.com/loom-network/plasma-cash-initial-release-plasma-backed-nfts-now-available-on-loom-network-sidechains-37976d0cfccd).

![divider](divider.png)

## 5. Zero Knowledge is coming

Over the past year the Ethereum developer community began to appreciate that new zero-knowledge technology will have a significant impact on blockchain technologies. Over the past 12 months, it has felt like every technical conversation in the Ethereum community takes the form of "well, we can do it this way for now, but of course once we have good zkSTARKs, it will be like this…".

Most people in the crypto industry will have heard of [zero-knowledge tech](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/), most famously used in the privacy cryptocurrency Zcash. But zero-knowledge technology won't just be used for privacy. It has important implications for many scalability techniques as well. Recent research and development into this technology (specifically, a class of zero-knowledge tech called zkSTARKs) may dramatically lower the computational cost required to use them in production, opening up new opportunities to integrate them with programmable blockchains like Ethereum.

In short, [zero-knowledge proofs](https://crypto.stackexchange.com/questions/12433/zero-knowledge-proof-protocol-example) let us prove that some operation happened, without having to share the underlying data. If the verification of that proof can be done cheaply enough, then it could let Ethereum smart-contracts verify that an operation took place off-chain. This means that we could, for instance, conduct [large numbers of operations off-chain, and then cheaply verify that they happened](https://ethresear.ch/t/on-chain-scaling-to-potentially-500-tx-sec-through-mass-tx-validation/3477). Or, we could conduct intensive computation off-chain, and still have it verified on-chain.

2018 was the year that the full potential of zero-knowledge tech started to sink in. In January, Eli Ben-Sasson & his co-authors [published their long-awaited paper on zkSTARKs.](https://www.coindesk.com/white-paper-trustless-privacy-tech-zk-starks-published) The Ethereum community began to work on how this technology can be used for scaling and in conjunction with other technologies, [like Plasma](https://ethresear.ch/t/plasma-is-plasma/2195). On the layer 1 side, developers made plans to ensure that ETH 2.0 has the requisite support for zkSTARKs, like [STARK-friendly hash functions](https://ethresear.ch/t/hash-based-vdfs-mimc-and-starks/2337).

New zkSNARK libraries were released, like iden3's [snarkjs](https://github.com/iden3/snarkjs) and [circom](https://github.com/iden3/circom), adding to existing libraries like [Zokrates](https://github.com/Zokrates/ZoKrates). In December 2018 a team at [ETHSingapore built a zkSNARK "rollup"](https://devpost.com/software/plasma-winter) scaling proof of concept, later released on testnet as the ([not technically Plasma](https://twitter.com/VitalikButerin/status/1082054495956291584)) [Plasma Ignis](https://twitter.com/TheMatter_io/status/1081959506454695936). BarryWhiteHat [contributed critical work](https://www.youtube.com/watch?v=lv6iK9qezBY) on using zkSNARKs on Ethereum. And Ben-Sasson & others launched [StarkWare Industries](https://www.starkware.co/).

![divider](divider.png)

## 6. The Road to ETH 2.0

ETH 2.0 is the name for the long-term research and development of the Ethereum platform, incorporating fundamental base-layer upgrades like [Proof of Stake](https://github.com/ethereum/wiki/wiki/Proof-of-Stake-FAQs) and [Sharding](https://github.com/ethereum/wiki/wiki/Sharding-FAQs).

The history of ETH 2.0, aka Serenity, has featured false starts, dead ends and more false starts. But in 2018, the long-term Ethereum roadmap began to solidify.

In January 2018, the [FFG testnet](https://hackmd.io/s/Hk6UiFU7z) launched, though it suffered from networking issues that made it difficult to use. A few months later however, the research direction moved away from FFG, and towards a plan that would see Casper and Sharding implemented together. In Q2, consensus began to form around what is now the [current plan](https://docs.ethhub.io/ethereum-roadmap/serenity-phases).

Explaining ETH 2.0 is beyond the scope of this post. If you want to get caught up, we recommend EthHub's summary [here](https://docs.ethhub.io/ethereum-roadmap/serenity-phases), [Vitalik's talk from DevconIV](https://youtu.be/kCVpDrlVesA), or [James Prestwich's recent guide](https://hackernoon.com/what-to-expect-when-eths-expecting-80cb4951afcd).

Once the research vision was clear, it was possible to [create a specification](https://github.com/ethereum/eth2.0-specs) for what became known as "ETH 2.0". This allowed [many different engineering teams](https://www.coindesk.com/next-gen-buidlers-the-8-teams-working-on-ethereum-2-0) to begin implementing that specification into client software. At the end of 2018, there were at least 8 teams building clients for ETH 2.0. Recently, Ben Edgington also began a [weekly newsletter which closely tracks the research and implementation of ETH 2.0](https://notes.ethereum.org/c/Sk8Zs--CQ).

While all roadmaps are subject to change and projections are uncertain, the beacon chain is expected to go live in 2019, with a beacon chain testnet scheduled to happen in the next few months. The beacon chain will allow ETH holders to choose to transfer their ETH to the beacon chain in order to earn rewards as a validator. However, that ETH cannot be transferred back to the "ETH 1" chain.

The next phase will include shards, which will be managed by the beacon chain. It's also possible that the [beacon chain will be used to finalize](https://ethresear.ch/t/using-the-beacon-chain-to-pos-finalize-the-ethereum-1-0-chain/4521) the current proof of work chain, somewhat similar to the way that FFG was once planned a year ago to be used for finalization.

While the roadmap has considerably firmed up, there are still [unsolved problems in blockchain sharding](https://medium.com/nearprotocol/unsolved-problems-in-blockchain-sharding-2327d6517f43). While the first few phases are relatively clear and there are no [significant unsolved theoretical problems left](https://www.youtube.com/watch?v=BkMZdbzKZ9k), plenty of interesting research and implementation problems remain for future phases so that we get to a truly scalable layer 1 of Ethereum.

![divider](divider.png)

## What did it all mean?

We warned you this post would be long. But it's still not comprehensive. A lot more happened in the Ethereum ecosystem this year, including a few developments worth noting quickly here:

* Ethereum core developers [came to rough consensus on a set of short-term upgrades](https://ethereum-magicians.org/c/working-groups/ethereum-1-x-ring) to the current Ethereum protocol ("Ethereum 1.X"), while ETH 2.0 is under development
* Regulators across the world [started paying attention to cryptocurrency](https://www.cnbc.com/2018/06/14/bitcoin-and-ethereum-are-not-securities-but-some-cryptocurrencies-may-be-sec-official-says.html), including securities regulators. Many jurisdictions are now in the process of deciding how digital assets, like the kind that can be created on Ethereum, are treated under law.
* Non-plasma sidechain technology, like [POA network](https://poa.network/) and [Parity-bridge](https://www.parity.io/bridging-the-dapp-scaling-now-with-parity-bridge/), launched into production
* UX made progress, like [Universal Logins](https://medium.com/@avsa/universal-logins-first-demo-1dc8b17a8de7) and [meta transactions](https://medium.com/@austin_48503/ethereum-meta-transactions-90ccf0859e84)
* The Ethereum Foundation [launched a grants program](https://blog.ethereum.org/2018/03/07/announcing-beneficiaries-ethereum-foundation-grants/) to fund critical work from across the community.

Should we view this year as a success, or a setback?

A strange thing about this moment in Ethereum's history is that you will receive wildly different answers depending on someone's frame of reference.

If your baseline is 2015–2016, you remember when Ethereum was still firmly an experiment, with virtually no users, developer tools, or even applications. The contrast with 2018 is startling. There are real applications now, live on mainnet, that provide real utility to their users — even if those user bases remain small. The thing we believed could happen, which may have once seemed impossible, is starting to happen, in bits and pieces.

But if your frame of reference is the hyped up narrative sold to you by ICO whitepapers and glossy keynote conferences, then it must be disappointing. Mass adoption not only has not yet arrived, but remains over the horizon. There are hard problems yet to be solved, and the technical progress zigs and zags, instead of following the comforting straight line of a tidy infographic roadmap.

Welcome to the real. There are experiments to be run, lessons to be learned, and [hard problems](https://www.lesswrong.com/posts/fpecAJLG9czABgCe9/on-doing-the-impossible) to solve. Grab a shovel, and see you next year.

—

**Josh Stark** ([L4](http://l4v.io/)), **Evan Van Ness** ([Week in Ethereum](http://weekinethereum.com/), [ConsenSys](https://consensys.net/)), and **Daniel Zakrisson** ([hardfork.se](https://www.hardfork.se/))

Thanks to Georgios Konstantopoulos, Jeff Coleman, Spencer Noon, Alex Wade, Xuanji Li, Danny Ryan, Heather Davidson, Gregor Zavcer, Mike McDonald, Corey Petty, Ameen Soleimani, Jens Frid, and others who took time to answer questions and contribute to the creation of this article.
