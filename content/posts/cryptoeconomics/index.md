+++
title = "Making Sense of Cryptoeconomics"
date = 2017-08-28T00:00:00
description = "Understanding the intersection of cryptography, economics, and mechanism design"
tags = ["cryptoeconomics", "ethereum", "bitcoin", "mechanism-design"]
draft = false

[params.cover]
image = "cover.png"
alt = ""
caption = "The Roman Aqueduct at Segovia, an early marvel of engineering"
+++

A few months ago Parker Thompson, a well known Silicon Valley VC, [tweeted](https://twitter.com/pt/status/871473661101850624) that "the concept of crypto-economics is stupid. It's economics. Inventing your own word is just an excuse to ignore well-understood concepts."

The term "cryptoeconomics" causes a lot of confusion. People are often unclear on what it is supposed to mean. The word itself can be misleading, as it suggests that there is a parallel "crypto" version of the whole of economics. This is wrong, and Parker is right to mock such a generalization.

In simple terms, cryptoeconomics is the use of incentives and cryptography to design new kinds of systems, applications, and networks. Cryptoeconomics is specifically about building things, and has most in common with [mechanism design](https://en.wikipedia.org/wiki/Mechanism_design) — an area of mathematics and economic theory.

Cryptoeconomics is not a subfield of economics, but rather an area of applied cryptography that takes economic incentives and economic theory into account. Bitcoin, ethereum, zcash and all other public blockchains are products of cryptoeconomics.

Cryptoeconomics is what makes blockchains interesting, what makes them different from other technologies. As a result of [Satoshi's white paper](https://bitcoin.org/bitcoin.pdf), we have learned that through the clever combination of cryptography, networking theory, computer science and economic incentives we can build new kinds of technologies. These new cryptoeconomic systems can accomplish things that these disciplines could not achieve on their own. Blockchains are just one product of this new practical science.

This article aims to explain cryptoeconomics in clear, simple terms. First, we examine bitcoin as an example of cryptoeconomic design. Second, we consider how cryptoeconomics relates to economic theory in general. Third, we look at three different areas of cryptoeconomic design and research that are active today.

## 1. What is cryptoeconomics? Bitcoin as a case study

Bitcoin is a product of cryptoeconomics.

Bitcoin's innovation is that it allows many entities who do not know one another to reliably reach consensus about the state of the bitcoin blockchain. This is achieved using a combination of economic incentives and basic cryptographic tools.

Bitcoin's design relies on economic incentives and penalties. Economic rewards are used to enlist miners to support the network. Miners contribute their hardware and electricity because if they produce new blocks, they are rewarded with amounts of bitcoin.

Second, economic costs or penalties are part of bitcoin's security model. The most obvious way to attack the bitcoin blockchain would be to gain control of a majority of the network's hashing power — a so-called [51 percent attack](https://bitcoin.stackexchange.com/questions/658/what-can-an-attacker-with-51-of-hash-power-do) — which would let an attacker reliably censor transactions and even change the past state of the blockchain.

But gaining control of hashing power costs money, in the form of hardware and electricity. Bitcoin's protocol intentionally makes mining difficult, meaning that gaining control of a majority of the network is extremely expensive — enough that it would be hard to profit from the attack. As of August 16, 2017, the [cost of a 51 percent attack on bitcoin](https://gobitcoin.io/tools/cost-51-attack/) would be around $1.88 billion in hardware and $3.4 million in electricity every day.

Without these carefully calibrated economic incentives, bitcoin wouldn't work. If mining did not come with a high cost, it would be easy to launch a 51 percent attack. If there were no mining reward, there would be no industry of people who buy hardware and pay for electricity to contribute to the network.

Bitcoin also relies on cryptographic protocols. [Public-private key cryptography](https://security.stackexchange.com/questions/25741/how-can-i-explain-the-concept-of-public-and-private-keys-without-technical-jargo) is used to give individuals safe, exclusive control of their bitcoin. [Hash functions](https://medium.com/@ConsenSys/blockchain-underpinnings-hashing-7f4746cbd66b) are used to "link" each block in the bitcoin blockchain, proving an order of events and the integrity of past data.

Cryptographic protocols like these give us the basic tools necessary to build reliable, secure systems like Bitcoin. Without something like public-private key infrastructure, we could not guarantee to a user that they have exclusive control over their bitcoin. Without something like hashing functions, nodes would not be able to guarantee the integrity of the history of bitcoin transactions contained in Bitcoin's blockchain.

Without the hardness of cryptographic protocols like hashing functions or public-private key cryptography, we would have no secure unit of account with which to reward miners — no confidence that our record of past accounts was authentic and exclusively controlled by a rightful owner. Without a carefully calibrated set of incentives to reward an industry of miners, that unit of account could have no market value because there would be no confidence that the system could persist into the future.

In this way, bitcoin's design requires an understanding of both cryptography and how incentives affect the security properties and functionality of systems built with cryptography. Cryptoeconomics is strange and counterintuitive. Most of us are not used to thinking of money as a design or engineering problem, nor are we used to economic incentive design being an essential component of a new technology. Cryptoeconomics requires us to [think about information security problems in economic terms](https://youtu.be/u6VSPD5TrP4?t=6m11s).

One of the most common mistakes in this industry is made by those who view blockchains only through a lens of computer science or applied cryptography. We have a strong tendency to prioritize the things we are most comfortable with, and see things outside of our domain of expertise as less important.

In blockchain technology, this leads many people to assume or abstract away the crucial role of economic incentives. This is one reason we see meaningless phrases like "[blockchains are trustless](https://medium.com/@ntmoney/trustless-is-a-misnomer-956066661b79)", "[bitcoin is backed only by math](https://bitcoin.org/en/faq#why-do-bitcoins-have-value)" or "[blockchains are immutable](https://www.coindesk.com/blockchain-immutability-myth/)." These are all wrong in their own way, but all have the effect of obfuscating the essential role of a large network of people whose necessary participation in the network is maintained through economic incentives.

Cryptoeconomic systems like bitcoin feel like magic to someone who views them only as a product of computer science, because bitcoin can do things that computer-science alone could never accomplish. Cryptoeconomics isn't magic — it's just interdisciplinary.

## 2. How does it relate to economics more generally?

The term cryptoeconomics can be misleading because it suggests a comparison to economics as a whole. This is part of what leads people like Parker to dismiss the term. Economics is the study of choice: how people and groups of people respond to incentives. The invention of cryptocurrency and blockchain technology does not require a new theory of human choice — the humans haven't changed. Cryptoeconomics is not the application of macroeconomic and microeconomic theory to cryptocurrency or token markets.

Cryptoeconomics has most in common with mechanism design, a field related to game theory. In game theory, we look at a given strategic interaction (a "game") and then try to understand the best strategies for each player, and the likely outcome if both players follow those strategies. For instance, we might use game theory to look at a negotiation between two firms, relations between countries or even evolutionary biology.

Mechanism design is often referred to as reverse game theory because we start with a desired outcome and then work backwards to design a game that, if players pursue their own self interest, will produce the outcome we want. For instance, imagine we are responsible for designing the rules of an auction. We have an objective that we want bidders to actually bid the real value they place on an item. To achieve this, we apply economic theory to design the auction as a game [where the dominant strategy for any player is to always bid their true value](https://en.wikipedia.org/wiki/Vickrey_auction#Proof_of_dominance_of_truthful_bidding). One solution to this problem is called a [Vickrey auction](https://en.wikipedia.org/wiki/Vickrey_auction#Proof_of_dominance_of_truthful_bidding), where bids are secret and the winner of the auction (defined as the player with the highest bid) only pays the second highest amount that was bid.

Cryptoeconomics, like mechanism design, focuses on designing and creating systems. Like in our auction example, we use economic theory to design "rules" or mechanisms that produce a certain equilibrium outcome. But in cryptoeconomics, the mechanisms used to create economic incentives are built using [cryptography and software](https://docs.google.com/presentation/d/1-2NMcrqWOvrjcDTjiYfLHc5cNNsMpzq6FodDVkfDNZE/edit#slide=id.g6eb8cd7660a986c30) and the systems we are designing are almost always [distributed or decentralized](https://medium.com/@VitalikButerin/the-meaning-of-decentralization-a0c92b76a274).

Bitcoin is a product of this approach. Satoshi wanted bitcoin to have certain properties — for instance, that it be able to reach consensus about its internal state and that it be censorship-resistant. Then, Satoshi set out to design a system that would achieve those properties, assuming people responded in rational ways to economic incentives.

Most often, cryptoeconomics is used to provide a security guarantee about a distributed system. For instance, we have a cryptoeconomic security guarantee that the bitcoin blockchain is secure against a 51 percent attack unless someone is [willing to spend a few billion dollars](https://gobitcoin.io/tools/cost-51-attack/). Or, in a state channel — a topic we discuss later — we can have a cryptoeconomic security guarantee that an off-chain process is nearly as secure and final as an on-chain transaction.

It is worth noting that mechanism design is not a panacea. There is a limit to how much we can rely on incentives to predictably shape future behaviour. As [Nick Szabo rightly points out](https://twitter.com/nickszabo4/status/882738070616809472), ultimately we are speculating about people's future mental states and making assumptions about how they react to certain incentives. A cryptoeconomic system's security guarantee depends in part on the strength of its assumptions about how people react to economic incentives.

## 3. Three examples of cryptoeconomics

There are at least three different kinds of systems being designed today that could be called "cryptoeconomic".

### Example 1: Consensus protocols

Blockchains are able to reach reliable consensus without having to rely on a central trusted party — a product of cryptoeconomic design. Bitcoin's solution, which we surveyed above, is called "proof-of-work" consensus because miners must commit work — in the form of hardware and electricity — in order to participate in the network and receive mining rewards.

Improving proof-of-work systems and designing alternatives to them is one active area of cryptoeconomic research and design. Ethereum's current proof-of-work consensus mechanism includes many variations and improvements on the original design, enabling [faster block times](https://blog.ethereum.org/2015/09/14/on-slow-and-fast-block-times/) and being more [resistant to the mining centralization that can result from ASICs](https://ethereum.stackexchange.com/questions/16811/is-ethereum-asic-resistant).

In the near future, ethereum plans to migrate to a "proof-of-stake" consensus protocol called Casper. This is an alternative to proof-of-work that does not require "mining" in the usual sense: there is no need for specialized mining hardware or huge expenditures of electricity.

Remember that the whole point of requiring miners to buy hardware and spend electricity is to impose a cost on miners, as a way of raising the cumulative cost of attempting a 51 percent attack sufficiently high that it becomes too expensive. The idea behind proof-of-stake systems is to use deposits of cryptocurrency to create the same disincentive, rather than real-world investments like hardware and electricity.

In order to mine in a proof-of-stake system, you must commit a certain amount of ether into a smart contract "bond." Just like in proof-of-work, this raises the cost of a 51 percent attack — an attacker would have to commit a very large amount of ether to successfully attack the network, which they would then lose forever.

Casper is being designed by [Vlad Zamfir](https://medium.com/@Vlad_Zamfir), [Vitalik Buterin](https://medium.com/@VitalikButerin), and others at the Ethereum Foundation. You can read more about the history of Casper's design [in this series of posts by Zamfir](https://medium.com/@Vlad_Zamfir/the-history-of-casper-part-1-59233819c9a9) or hear him talk about it on a [recent podcast](https://www.youtube.com/watch?v=9nQPcNY32JQ). Buterin wrote a long post about Casper's design philosophy [here](https://medium.com/@VitalikButerin/a-proof-of-stake-design-philosophy-506585978d51), and there is a useful FAQ on the ethereum GitHub wiki [here](https://github.com/ethereum/wiki/wiki/Proof-of-Stake-FAQ).

### Example 2: Cryptoeconomic application design

Once we have solved the fundamental problem of blockchain consensus, we are able to build applications that sit "on top" of a blockchain like ethereum. The underlying blockchain gives us (1) a unit of value that can be used to create incentives and penalties, and (2) a toolkit with which we can design conditional logic in the form of "[smart contract code](https://www.coindesk.com/making-sense-smart-contracts/)." The applications we build with these tools can also be a product of cryptoeconomic design.

For instance, the prediction market [Augur](https://www.augur.net/) requires cryptoeconomic mechanisms in order to function. Using its native token REP, Augur creates a [system of incentives](http://blog.augur.net/faq/how-does-reputation-rep-work/) that rewards users for reporting the "truth" to the application, which is then used to settle bets in the prediction market. This is the innovation that makes a decentralized prediction market possible. Another prediction market, [Gnosis](https://gnosis.io/), uses a similar method, though also lets users specify other mechanisms for determining true outcomes (commonly called "oracles").

Cryptoeconomics is also applied to design token sales or ICOs. Gnosis, for instance, [used a "Dutch auction"](https://blog.gnosis.pm/introducing-the-gnosis-token-launch-3cc4cffb5098) as a model for its token auction, on the theory that this would result in a more fair distribution (an experiment that had [mixed results](http://vitalik.ca/general/2017/06/09/sales.html)). We mentioned earlier that one area where mechanism design has been applied is in the design of auctions, and token sales gives us a new opportunity to apply some of that theory.

These are a different kind of problem than building the underlying consensus protocols, but they share enough similarities that both can be fairly seen as cryptoeconomic. Building these applications requires an understanding of how incentives shape users' behaviour and careful design of economic mechanisms that can reliably produce a certain result. They also require an understanding of the capabilities and limitations of the underlying blockchain on which the application is built.

Many blockchain applications are not products of cryptoeconomics; for instance, applications like [Status](https://status.im/) and [MetaMask](https://metamask.io/) — wallets or platforms that let users interact with the ethereum blockchain. These do not involve any additional cryptoeconomic mechanisms beyond those that are already part of the underlying blockchain.

### Example 3: State channels

Cryptoeconomics also includes the practice of designing much smaller sets of interactions between individuals. The most notable of these are [state channels](http://www.jeffcoleman.ca/state-channels/). State channels are not an application but a valuable technique that can be used by most blockchain applications to become more efficient.

A fundamental limitation of blockchain applications is that blockchains are expensive. Sending transactions requires fees, and using ethereum to run smart-contract code is [comparatively costly](https://hackernoon.com/ether-purchase-power-df40a38c5a2f) to other kinds of computation. The idea behind state channels is that we can make blockchains more efficient by moving many processes off-chain, while still retaining a blockchain's characteristic trustworthiness, through the use of cryptoeconomic design.

Imagine Alice and Bob want to exchange a large number of small payments of cryptocurrency. The normal way for them to do this would be to send transactions to the blockchain. This is inefficient — it requires paying transaction fees and waiting for the confirmation of new blocks.

Instead, imagine that Alice and Bob sign transactions that [could be submitted to the blockchain, but are not](http://www.jeffcoleman.ca/state-channels/). They pass these back and forth between one another, as fast as they want — there are no fees at this point, because nothing is actually hitting the blockchain yet. Each update "trumps" the last one, updating the balance between the parties.

When Alice and Bob have finished exchanging small payments, they "close out" the channel by submitting the final state (i.e. the most recent signed transaction) to the blockchain, paying only a single transaction fee for an unlimited number of transactions between themselves. They can trust this process because both Alice and Bob know that each update passed between them could be sent to the blockchain. If the channel is properly designed, there is no way to cheat — say, by trying to submit a previous update as though it were the most recent — since recourse to the blockchain is always available.

For illustrative purposes, you can think of this as similar to how we interact with other trusted sources, like a legal system. When two parties sign a contract, most of the time they never need to take that contract to court and ask a judge to interpret and enforce it. If the contract is properly designed, both parties simply do what they promised to do, and never interact with the courts at all. The fact that either party could go to the court and have the contract enforced is enough to make the contract useful.

This technique is not just useful for payments, but for any update to the state of an ethereum program — hence the more general term "state channel" rather than the narrow "payment channel." Instead of sending payments back and forth, we can send updates to a smart contract back and forth. We can even send entire ethereum smart contracts that, if needed, will be sent to the blockchain and executed. These programs never have to be executed to be useful. All that is needed is a sufficiently high guarantee that they [could be executed if necessary](https://github.com/ledgerlabs/state-channels/wiki/Counterfactual-Terminology).

In the future, most blockchain applications will use state channels in some form. It is almost always a strict improvement to require less on-chain operation, and many things done on-chain today can be moved into state channels while still preserving a sufficiently high guarantee to be useful.

The description above skips over many important details and nuances of how state channels work. For a more detailed description, Ledger Labs [built a toy implementation last summer](https://github.com/ledgerlabs/state-channels/wiki/Example-State-Channel) that demonstrates the basic concept.

## Conclusion

Thinking about the blockchain space through the lens of cryptoeconomics is helpful. Once you understand the idea, it helps to clarify many of the controversies and debates in our industry.

For instance, "permissioned" blockchains that are centrally managed and do not use proof-of-work have been a source of constant controversy since they were first proposed. This area of work is often referred to as "distributed ledger technology" and is focused on financial and enterprise use cases. [Many partisans of blockchain technology dislike them](https://www.reddit.com/r/Bitcoin/comments/316sdy/to_ibm_stop_this_blockchain_nonsense_it_will/) — they may be blockchains in the literal sense, but there is something about them that feels wrong. They seem to reject the thing that many people see as the whole point of blockchain technology: being able to produce consensus without relying on a central party or traditional financial systems.

A cleaner way to make this distinction is between blockchains that are products of cryptoeconomics and blockchains that are not. Blockchains that are simply distributed ledgers and do not rely on cryptoeconomic design to produce consensus or align incentives might be useful for some applications. But they are distinct from blockchains whose whole purpose is to use cryptography and economic incentives to produce consensus that could not exist before, like bitcoin and ethereum. These are two different technologies, and the clearest way of distinguishing between them is whether or not they are products of cryptoeconomics.

Secondly, we should expect that there will be cryptoeconomic consensus protocols that do not rely on a literal chain of blocks. Obviously, such a technology would have something in common with blockchain technology as we call it today, but labelling them blockchains would be inaccurate. Again, the relevant organizing concept is whether such a protocol is the product of cryptoeconomics, not whether it is a blockchain.

The ICO craze has also focused attention on this distinction, though few have articulated it clearly. [Many](https://news.21.co/thoughts-on-tokens-436109aabcbe) [people](https://thecontrol.co/tokens-tokens-and-more-tokens-d4b177fbb443) [independently](https://medium.com/@datarade/criterion-for-high-fidelity-token-sales-1391ff20af20) [identified](https://www.coindesk.com/framework-valuing-crypto-tokens/) that one of the strongest signs of a token's value is whether it forms a necessary component of the application to which it is connected. To put this in clearer terms, the question should be: is the token part of a necessary cryptoeconomic mechanism in the application? Understanding the mechanism design of a project holding an ICO is an essential tool in determining that token's utility and likely value.

In the past years, we've moved from thinking about this new field solely through the lens of one application (bitcoin), to thinking about it in terms of one underlying technology (blockchains). What needs to happen now is to step back once again and view this industry in terms of a unifying approach to solving problems: cryptoeconomics.

---

*Thanks to Jeff Coleman, Ethan Wilding, and Vlad Zamfir for their comments on an earlier draft of this article.*
