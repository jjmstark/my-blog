+++
title = "Part 2 — Making Sense of Smart Contracts"
date = 2016-06-15T00:00:00
description = "Understanding the different definitions and uses of smart contracts"
tags = ["smart-contracts", "ethereum", "blockchain", "law"]
draft = false
+++

A [version of this article first appeared in Coindesk](http://www.coindesk.com/making-sense-smart-contracts/) on June 4, 2016.

Read Part 1 of this series [here](https://medium.com/@jjmstark/introduction-to-smart-contracts-part-1-8f191a324d0a#.dtzaa9z2s).

The term ["smart contract"](http://www.coindesk.com/research/smart-contracts-report/) has no clear and settled definition. The idea has long been hyped to the public as a central component of next-generation blockchain platforms, and as a key capability for any practical enterprise application.

They are defined variously as ["autonomous machines"](http://motherboard.vice.com/read/smart-contracts-sound-boring-but-theyre-more-disruptive-than-bitcoin), ["contracts between parties stored on a blockchain"](http://en.finance.sia-partners.com/impact-blockchains-smart-contracts-insurance) or ["any computation that takes place on a blockchain"](http://www.multichain.com/blog/2015/11/smart-contracts-good-bad-lazy/). Many [debates about the nature of smart contracts](https://www.reddit.com/r/Bitcoin/comments/300yez/if_it_doesnt_escrow_value_its_not_a_smart_contract/) are really just contests between competing terminology.

The different definitions usually fall into one of two categories. Sometimes the term is used to identify a specific technology — code that is stored, verified and executed on a blockchain. Let's call this type of definition "smart contract code".

Other times, the term is used to refer to a specific application of that technology: as a complement, or substitute, for legal contracts. Let's name these "smart legal contracts".

Using the same term to refer to distinct concepts makes answering even simple questions impossible. For instance, one question I'm often asked is simply: what are the capabilities of a smart contract?

If we are talking about smart contract code, then the answer depends on the capabilities of the language used to express the contract and the technical features of the blockchain on which it operates.

But if we are asking about using that technology to create a binding legal agreement, or an effective substitute for a binding legal agreement, the answer depends on far more than the technology. This answer depends on existing legal doctrine and how our legal, political and commercial institutions decide to treat the technology. If businesspeople don't trust it, the legislature doesn't recognize it and the courts can't interpret it, then it won't be a very practically useful "contract".

It would be futile to try and change the way people use the term already. Practically speaking, we are probably stuck using — or at least reading — the term "smart contract" for now. This makes it essential for anyone interested in this space to understand the different ways the term is used and be able to distinguish clearly between them.

## Smart contracts as smart contract code

Blockchains can run code. While the first blockchains were designed to perform a small set of simple operations — mainly, transactions of a currency-like token — techniques have been developed to allow blockchains to perform more complex operations, defined in full-fledged programming languages.

Because these programs are run on a blockchain, they have unique characteristics compared to other types of software. First, the program itself is recorded on the blockchain, which gives it a blockchain's characteristic permanence and censorship resistance. Second, the program can itself control blockchain assets — i.e., it can store and transfer amounts of cryptocurrency. Third, the program is executed by the blockchain, meaning it will always execute as written and no one can interfere with its operation.

To developers and others working directly with blockchain technology, the term "smart contracts" is most often used to refer to this blockchain code. You'll see this use of the term in the [Ethereum documentation](https://ethereum-homestead.readthedocs.io/en/latest/), on [stackexchange](http://ethereum.stackexchange.com/questions/607/how-to-unit-test-smart-contracts) and in [technically minded articles](http://www.coindesk.com/three-smart-contract-misconceptions/). The term has been particularly associated with the Ethereum project, whose primary purpose is to be a platform for smart contract code. But today, the term is used generically [across](http://www.coindesk.com/smart-contract-1-million-bitcoin-rootstock/) [the](https://docs.erisindustries.com/explainers/smart_contracts/) [community](https://medium.com/@tjayrush/smart-contracts-are-immutable-thats-amazing-and-it-sucks-e0fbc7b0ec16#.sl3xvhf0w) to refer to any complex program that is stored and executed on a blockchain.

Calling these programs contracts is helpful in that this code is governing something important or valuable. We only go to the trouble of creating a binding contract when it's important that we be able to enforce the terms. Similarly, we only use smart contract code when the code controls something important, like money or identity.

That said, smart contract code need not resemble anything we would ordinarily think of as a "contract". While the code could articulate a conditional financial transaction ("send 1 BTC from Alice to Bob on July 1, 2016"), it could also be a governance application that controls account permissions ("if Alice has voted yes, remove Bob's voting rights over Application X and notify the following accounts…").

In many cases, smart contract code is not used in isolation but as a small piece in a larger application. Every DApp, DAO, or other blockchain-based application is built using smart contract code to perform operations on their chosen blockchain. Any Ethereum application that you've read about — like [Augur](http://augur.net/), [Slock.it](http://slock.it/), or [Boardroom](http://boardroom.to/) — is made out of smart contract code.

## Imperfect, misleading, and someday outdated

The term receives a lot of valid criticism. Relying on the metaphor of a "contract" is misleading because it emphasizes a single narrow use case. The term fails to capture one of the key capabilities of blockchain programs: that they have a kind of independent agency.

Smart contract programs can themselves hold balances of cryptocurrency, or even control other smart contract programs. Once they are created, they can act autonomously when called to perform an action. For this reason, many prefer the term "smart agent", analogous to the more general concept of a [software agent](https://en.wikipedia.org/wiki/Software_agent).

Eventually, this use of the term may simply fade from use as blockchain technology matures.

Developers will be more likely to refer to a specific language ("Let's look at your [Solidity code](https://solidity.readthedocs.io/en/latest/)") or platform ("Our application runs on [Eris.db](https://erisindustries.com/components/erisdb/)") that they are working with, as opposed to a generic term that could describe any complex operation on a blockchain.

The capabilities and purpose of smart contract code as distinct from other code may simply become clear from context, without requiring the use of a clumsy analogy like "contract". It might end up being more similar to how we speak of HTML and JavaScript today, without having to think about how the former is a "markup" language, playing a distinct role from JavaScript in the overall web application.

## Smart contracts as smart legal contracts

Among those who work in finance or law, the term "smart contract" is often read quite differently than the definition above.

"Smart contract" here refers to a specific use case of smart-contract code — a way of using blockchain technology to complement, or replace, existing legal contracts. This is the definition of the term I considered in [my last piece](http://www.coindesk.com/blockchain-smarts-contracts-real-world-law/): the use of code to articulate, verify, and enforce an agreement between parties. A smart legal contract.

These smart legal contracts would most likely be a combination of smart contract code and more traditional legal language. For instance, imagine a supplier of goods enters into a smart legal contract with a retailer. The payment terms could be defined in code and executed [automatically when delivery is made](https://www.loaddelivered.com/blog/why-blockchain-is-a-game-changer-for-supply-chain-management/). But the retailer would likely insist the contract include an [indemnity clause](https://en.wikipedia.org/wiki/Indemnity), whereby the supplier agrees to indemnify the retailer against claims flowing from a defective product. There would be no point representing this clause in code, since it is not something that can self-execute — it exists to be interpreted and enforced by a court in the case of litigation.

Commercial agreements are full of boilerplate clauses that protect parties from various edge-case liabilities, and these are not always suitable for representation and execution through code, meaning that smart legal contracts will require (at least for the foreseeable future) a blend between code and natural language.

This is the basic idea behind Eris Industries' [dual integration](https://erisindustries.com/components/erislegal/) system, Primavera de Fillipi's proposed [Legal Framework for Crypto-Ledger Transactions](http://p2pfoundation.net/Legal_Framework_For_Crypto-Ledger_Transactions), and R3's Corda [smart contracts system](http://www.coindesk.com/barclays-smart-contracts-templates-demo-r3-corda/).

Could smart legal contracts ever be considered legally enforceable? Probably. Despite what many think, the conditions under which an agreement becomes a legally enforceable contract are flexible and attuned to the underlying relationship between the parties, rather than dependent on the form the contract takes. Anything from a verbal agreement to an email conversation can become a contract at law, if the [basic elements of a contract can be found](https://medium.com/@ConsenSys/unpacking-the-term-smart-contract-e63238f7db65#.nak50tdkj).

## Many contracts, many use cases

The category of smart legal contracts is complicated by the fact that there are many different types of contracts in the world, only some of which are obvious candidates for use as "smart contracts". A legal contract could be anything from a verbal agreement for someone to paint your house to a derivative traded electronically in financial markets.

Since early 2015, the use cases attracting the most attention are [smart legal contracts as smart financial instruments](https://www.dlapiper.com/en/us/insights/publications/2016/04/the-blockchain-revolution/) like shares, bonds, or derivatives contracts. Articulating these contracts in code could allow financial markets to become more automated and simplify many process-intensive systems related to trading and servicing of financial instruments.

These "smart financial instruments" do not exist at scale today, although many people are working to build them. R3's recently announced [Corda platform](http://www.coindesk.com/9-takeaways-r3s-new-distributed-ledger-tech/) is designed to facilitate this type of smart-contract. Digital Asset Holdings [recently acqui-hired Elevance](http://www.coindesk.com/digital-asset-acquires-elevence/), a Swiss firm that has developed a way to model financial agreements in code. In April, Barclays' [revealed details of a scheme](http://www.cnbc.com/2016/04/19/barclays-used-blockchain-tech-to-trade-derivatives.html), in cooperation with R3, to represent ISDA agreements in smart contract code.

Financial instruments are just one type of contract that could benefit from blockchain code. As the technology matures, other assets — e.g. real estate, or intellectual property — may be stored and traded over blockchain systems. As new asset types go "on-chain", the agreements used to govern those assets in the world today (like a mortgage or licensing agreement) may benefit from blockchain-based analogs.

## Alternatives to traditional legal agreements

Many advocates for blockchain technology see larger possibilities. Rather than merely imitate or complement the legal contracts we use today, perhaps smart contract code could be used to facilitate new types of commercial arrangements.

We might even call this a third definition of the term: using smart contract code to create novel, alternative forms of agreements that are nonetheless commercially useful. Let's call these "smart alternative contracts".

This approach takes a broader view of the real-world problem solved by contracts. Commerce depends on individuals being able to form stable, predictable agreements with one another. Contracts, along with a strong legal system, are the primary mechanisms we use to shape each party's incentives to the point where they have sufficient confidence in their relationship to engage in the risky business of trade.

But perhaps legal agreements are not the only solution to this general problem. Smart contract code offers a new set of tools to articulate and enforce terms, and they can be used to create systems of incentives that may be sufficient to make commercial relationships possible.

The most widely discussed opportunity of this type is machine-to-machine commerce. The growing ecosystem of smart devices — particularly those that are in some fashion autonomous — will eventually need a way to engage in basic commercial interactions with one another. For instance, a washer that [buys its own detergent](http://www.coindesk.com/ibm-reveals-proof-concept-blockchain-powered-internet-things) or a [car that can pay to recharge itself](http://www.coindesk.com/german-utility-company-turns-to-blockchain-amid-shifting-energy-landscape/).

These transactions still require a minimum level of trust to be commercially viable, but are ill-suited for legal contracts, which are comparatively expensive and require the involvement of legal persons like a corporation or human. Smart alternative contracts might enable an entirely new type of commerce carried out between our computers, cars, phones, and appliances.

There probably are — or will be — other types of commercial interaction that aren't well suited to traditional legal contracts. New markets, suddenly made possible by technology, but which are underserved by legal tools that are slow to innovate and adapt.

Smart alternative contracts might let us stretch the web of trust out a little further, a little faster, beyond the reach of the legal system, where they can enable new forms of commerce not possible today.

## Conclusion

The lack of clear terminology in this field is an unfortunate reality. Those of us who work in the blockchain space should be mindful of how the term is being used in different communities, and be prepared to ask a series of annoying, though necessary, clarifying questions when asked about the nature and potential of "smart contracts".

The different uses of the term illustrate a broader challenge in our industry. The interdisciplinary nature of blockchain technology, and "smart contracts" in particular, lead people to see the technology as primarily belonging to their own discipline, at the expense of the others. Lawyers often look at smart contracts and see marginally improved legal agreements, without appreciating the fuller potential of blockchain-code to extend beyond law's reach.

Developers, on the other hand, consider smart contracts and see the limitless possibilities of software, without appreciating the subtleties and commercial realities reflected in traditional legal agreements.

As with any interdisciplinary field, both must learn from the other.

---

*Josh Stark (J.D. U of T) is a lawyer and head of Operations & Legal at [Ledger Labs](http://ledgerlabs.io/), a blockchain consulting firm and development group.*
