+++
title = "Brief responses to two USV Ethereum Critiques"
date = 2019-09-09T00:00:00
description = "Brief responses to two USV Ethereum Critiques"
tags = ["ethereum"]
draft = false

+++

Two partners at Union Square Ventures recently published separate blogs critical of Ethereum: "[Is Ethereum the AOL of Crypto?](https://continuations.com/post/187279569830/is-ethereum-the-aol-of-crypto)" by Albert Wenger, and "[Some Thoughts on Crypto](https://avc.com/2019/09/some-thoughts-on-crypto/)" by Fred Wilson.

I'm fond of saying that "[Ethereum needs better critics](https://twitter.com/0xstark/status/1078758860205289477?s=20)". Hopefully Albert and Fred continue being critics, and through debate with the Ethereum community, become better ones over time. A positive trait in the Ethereum community is our interest in [deliberately seeking out flaws, exposing them](https://medium.com/@ameensol/what-you-should-know-before-putting-half-a-million-dai-in-compound-fafdb2645f77), and fixing them.

The explicit goal of this short post is to bait Albert and Fred into being better critics. Expand on your arguments, tell us (beyond generalities) what you think Ethereum is doing wrong, and what others are doing better.

Ethereum isn't perfect. If it was perfect, what would there be to do? Ethereum has many flaws, but it has incredible potential. This means there are many interesting problems to solve, and that solving those problems matters.

## "Is Ethereum the AOL of Crypto?" by Albert Wenger

The gist of Albert's [post](https://continuations.com/post/187279569830/is-ethereum-the-aol-of-crypto) is that one area of activity on Ethereum, Decentralized Finance (or "Open Finance" if you prefer) may be circularly dependent on a small segment of the Ethereum community for both its funding and its users. There are two arguments there, which I'll do my best to [steelman](https://wiki.lesswrong.com/wiki/Steel_man):

### 1. Is DeFi dependent on Ethereum for funding?

Albert's first argument goes like this: DeFi has been a success for Ethereum so far. However, if it is the case that most DeFi companies are being financed "by Ethereum", then it may create a circular dependency that could be undone by some adverse event, similar to how the dot-com bust undid AOL. For instance, if most DeFi companies are being funded by large ETH holders selling ETH, and those companies were to fail, this could lower the price of ETH. This in turn would mean there is less funding available for new DeFi companies, meaning less success, meaning a lower ETH price, and on and on.

The obvious question is simply: is it true that a lot of DeFi is "financed via Ethereum"?

Albert gives two examples of what he means by this:

* When a DeFi project has its own token. I assume the point here is that a project with its own token is financially dependent on the price of that token, which we assume might be correlated with the price of ETH. Such a project might also simply hold a lot of ETH.
* When a DeFi project is financially supported by organizations or people with large holdings of ETH (e.g. ConsenSys, which he calls out specifically).

Surveying the DeFi industry, Albert's claim seems mostly false. Most of the top DeFi projects (1) do not have their own token, and (2) have raised (and continue to raise) outside VC capital.

To use one metric, out of the 10 top DeFi projects listed on [DeFi Pulse](https://defipulse.com/):

* 4 have their own token (MakerDAO, Synthetix, Bancor, Kyber)
* 8 have raised VC money (MakerDAO, Compound, Synthetix, dYdX, Uniswap, Set, Dharma, wBTC (via Kyber), Bancor, and Kyber)
* 1 raised money from ConsenSys (Nuo)

This doesn't include other stablecoins like USDT, USDC, Gemini, and others — all funded by VC and large exchanges.

It doesn't seem true that DeFi is being propped up by large ETH holders. What companies or projects is Albert thinking of when he writes this critique, if not the ones listed above?

### 2. Is DeFi dependent on a small circular economy of users?

Separate from the AOL analogy, Albert is getting at a deeper question: is it dangerous that so much of DeFi is "self-referential" within Ethereum?

Traders who want leverage are the primary consumers of lending products, borrowing from ETH holders. Financial services and products (derivatives, trading services, etc) let users interact with or have exposure to a variety of ETH based assets, and some of those assets have little use outside of speculation.

Whether you view the above description as a strike against DeFi probably depends on your frame of reference. On the one hand, it's true that the lofty vision of a global alternative financial system that banks the unbanked and provides accessible financial services to the world is far from reality.

On the other hand, what should we expect? Ethereum launched 5 years ago, Dai has existed for under 2 years, and DeFi as a proper noun is about 1 year old. Shouldn't we expect an emergent financial system to begin as a very local phenomenon, while basic infrastructure and services are laid down, before expanding its scope? Even then, isn't some amount of self-reference a good thing, since it creates demand for ETH?

It's not even really true that DeFi is entirely walled off within Ethereum: see for instance efforts to integrate with Bitcoin like [wBTC](https://www.wbtc.network/) and [tBTC](https://tbtc.network/), or the many companies working to bridge Ethereum to the legacy financial system (here [are](https://www.coindesk.com/crypto-and-security-token-exchange-inx-to-raise-130-million-in-landmark-ipo) [three](https://www.theblockcrypto.com/tiny/visa-debit-card-available-in-europe-allows-to-spend-dai-stablecoin-anywhere-in-the-world/) [examples](https://www.coindesk.com/national-stock-exchange-becomes-worlds-first-to-list-a-tokenized-security?utm_source=twitter&utm_medium=coindesk&utm_term=&utm_content=&utm_campaign=Organic+) just from the last month). DeFi's integration with other ecosystems is just as true at the social level: Bitfinex, a company whose culture is very Bitcoin-centric, used Ethereum for their token sale.

## "Some Thoughts on Crypto" by Fred Wilson

Fred's [piece](https://avc.com/2019/09/some-thoughts-on-crypto/) is a bit lighter, and has only a few remarks about Ethereum.

Fred's claims are simple: Ethereum is hard to build on, it's hitting scaling challenges, and "many developers are looking elsewhere."

Yes, Ethereum's developer experience still needs improvement. This has been, and remains, a large priority for the community. But while development on Ethereum is frustrating relative to established areas of software development, it is dominant over every other smart contract platform. Don't take my word for it — [ask projects who have tried to build on other chains](https://blog.synthetix.io/cross-chain-infrastructure-revisited/) or [incubators who target blockchain startups](https://twitter.com/yossihasson/status/1169571179650322433).

Yes, some developers are looking at other platforms. They should! It would be irresponsible for any entrepreneur or developer not to kick the tires and figure out the best stack for their needs. Especially when many (not yet launched) chains are making incredible claims about their (theoretical) performance.

But so far, when developers are voting with their [money](https://twitter.com/spencernoon/status/1151214732684222465) and time, the [vast majority of them](https://www.electriccapital.com/electric-research) are still choosing Ethereum:

In terms of distribution, [Ethereum remains the IBM of our ecosystem.](https://www.placeholder.vc/blog/2019/8/31/ethereum-and-the-seven-dwarfs) As more competing chains come online and begin spending their warchests, the Ethereum ecosystem might bleed a few developers. The difference between Ethereum and its competitors is that Ethereum actually has developers at risk of leaving.

The important question isn't whether some developers build on other platforms, but whether any other chain can displace Ethereum as the de-facto smart contract platform used by the majority of the industry. Does Fred think this is likely? If so, why specifically?

As for scaling challenges — Ethereum is absolutely running up against these — an unfortunate side effect of having developers and users on your platform! Your view on whether those challenges are insurmountable will depend on your view of the adoption of layer 2 scaling tech and progress on ETH 2.0, topics too large to cover here.

The reason Fred's piece touched a nerve isn't these points by themselves, which are relatively obvious and well-understood concerns. What set people off was the strange contrast between his disappointment in Ethereum and his other comments.

For instance, his very next point in the blog post is that "Stablecoins […] are a bright spot". On twitter, [I pointed out](https://twitter.com/0xstark/status/1169280255254679552) that virtually every stablecoin with any use is an ERC-20, which seems at odds with his dim view of Ethereum. Fred [clarified](https://twitter.com/fredwilson/status/1169288109151924224) that his concern is that they might "leave" Ethereum.

Many stablecoins probably will launch alt-versions of themselves on other chains eventually, but it's hard to imagine why a project would abandon all of the capital, users, infrastructure, services, and liquidity available to their ERC-20s. Until there is any evidence that developers or users are abandoning Ethereum, isn't the success of stablecoins — virtually all built on Ethereum — a point in its favour?

I am curious what specific weaknesses of Ethereum and specific strengths of its imitators motivated Fred's post. But it's hard to know what to make of his conclusions right now.

If Ethereum is doing everything wrong, why is the entire crypto industry building on it? Between Fred publishing his post, and my sitting down to draft this one, [Binance announced plans to launch a USD stablecoin](https://www.theblockcrypto.com/2019/09/05/binance-launching-its-own-usd-pegged-stablecoin-busd-with-paxos-as-custodian/), and [Paxos announced a gold-backed token](https://www.theblockcrypto.com/2019/09/05/paxos-embraces-gold-pegged-crypto-as-sea-change-in-gold-trading/).

Both will be built on Ethereum.

---

*Thanks to Eric Conner, Ryan Sean Adams, Evan Van Ness, and others for their feedback on this post.*
