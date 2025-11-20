+++
title = "Introduction to Smart (legal?) Contracts"
date = 2025-11-14T14:17:47.363402
draft = false

[params.cover]
image = "acb1f3aa-490b-4898-864b-3024ec0cdc8a.png"
alt = "Introduction to Smart (legal?) Contracts — Josh Stark"
caption = "Introduction to Smart (legal?) Contracts — Josh Stark"
+++


Introduction to Smart (legal?) Contracts

Josh Stark

0x4aa9

September 17th, 2021

*👋 Note: Originally published in April 2016 on [Coindesk](https://www.coindesk.com/markets/2016/04/11/how-close-are-smart-contracts-to-impacting-real-world-law/) and [Medium](https://jjmstark.medium.com/introduction-to-smart-contracts-part-1-8f191a324d0a).*

Over the last year, the concept of a “smart contract” has received renewed attention in both the technology industry and in legal and business circles. Recent advancements in a field known as “blockchain technology” have led some to believe that smart contracts could soon offer alternatives to traditional commercial and financial agreements, with dire results for the legal and financial sectors. While this enthusiasm may be premature, lawyers nonetheless remain mostly unaware of this important emerging technology and the long-term implications for their profession.

In this context, “smart contract” refers specifically to the use of computer code to articulate, verify, and execute an agreement between parties. Whereas a typical contract is drafted using natural language, the terms of smart contracts are expressed in code, similar to a programming language like javascript or HTML. The contract is then “executed” by a computer — given the conditions of the agreement, and a set of defined inputs, the smart contract enforces its own terms.

Readers familiar with blockchain technology will know that the term “smart contract” is often used in a more general sense to refer to any script or program that operates on a blockchain. However for the purposes of this article, I focus on the narrower meaning described above: using code in place of traditional contractual agreements between parties.

---

The term “smart contract” was first popularized by computer scientist Nick Szabo in his 1997 paper *The Idea of Smart Contracts*. The vending machine, he described, is the simplest form of a “smart contract” — a mechanical device designed to transfer ownership of a good (a candy bar) when provided with a certain defined input ($1.50). Because the machine itself “controls” the property — by being physically sealed — it is able to enforce the terms of the “contract”.

Extending the concept, Szabo suggested that computer code could be used in place of mechanical devices to facilitate far more complex transactions of *digital* property. Rather than transfer ownership of a candy bar, a smart contract could transfer ownership of real-estate, or shares, or intellectual property. The program would define what “inputs” were necessary for the contract to execute — things like payment, or votes of board members, or any other condition that can be expressed by code.

Consider a basic options contract. A call options contract entitles the holder to buy a given security at a defined price. In our example, Alice buys our “smart options contract” from Bob. The contract entitles Alice to purchase 100 shares of Acme Inc. from Bob at a defined price of $50 per share. The contract has an expiry date, after which Alice is no longer entitled to buy the share at the defined “strike price”.

Expressed in pseudo-code, a simple “smart options contract” might look like this:

```
contract Option {   strikePrice = $50
   holder = Alice
   seller = Bob
   asset = 100 shares of Acme Inc.
   expiryDate = June 1st, 2016   function exercise ( ) {

             If Message Sender = holder, and
      If Current Date < expiryDate, then
         holder send($5,000) to seller, and
         seller send(asset) to holder
   }

}
```

In the first section, the smart options contract defines the relevant terms — the underlying asset, the strike price, the identities of each party, and the expiry date. Then, a function we’ve named “exercise” enables the holder to trigger the purchase of shares at the strike price at any moment before the expiry date. The function first checks to see if the entity triggering it (the “Message Sender”) is the holder, and then checks to see that the contract is still within the expiry date. If both are true, then the contract immediately executes by transferring cash from the holder to the seller, and the assets from the seller to the holder, according to the contract’s terms.

---

Until recently, smart contracts were little more than theory. In general, there were two fundamental challenges that needed to be addressed before smart contracts could be used in any real-world setting.

**(1)** How would a smart contract actually *control* real assets so that it could enforce an agreement? A vending machine, to return to Szabo’s example, controls property by physically securing it inside of itself. But how could code do the same? In our options contract above, the “exercise” function transfers money and assets between the two parties. But how can a computer program control real-world assets like cash and shares?

**(2)** What computer would be trusted to “execute” those terms in a way that both parties could rely upon? Parties must not only agree on the code of their contract, but also the computer which interprets and executes that code. A shared standard, at the minimum, would have to exist, and be used in a way that was verifiable by each party — ideally, without requiring the parties to physically inspect the computer in question.

In the last few years, solutions to both of these problems have come into sight. Emerging research and development surrounding what is called “blockchain technology” may provide a basis to make smart contracts a reality in the near future.

The first use of blockchain technology was the digital currency bitcoin, made famous by its mysterious creator and sudden price increase in late 2013. In the last few years, the underlying “blockchain” technology has been intensely studied and adapted to expand its use beyond simple digital currencies. Startups, open-source communities, and large financial institutions alike are improving and expanding the technology with the aim of one day using it to facilitate exchange of fully digital assets.

A blockchain is an **authoritative database**. It is a database that, by virtue of the way it is maintained and updated, has very high trust properties. Blockchains are not controlled by a single party. There is no single company, organization, or person that has ultimate control over a blockchain. Rather, a blockchain is maintained, updated, and secured by a network of participating computers.

Each computer keeps a full copy of the blockchain database, and each copy is kept in synchronization with the others by a system of cryptographically-enforced rules called a *consensus algorithm*. Crucially, blockchains are *append-only* databases, meaning that once information is validly added, it can never be removed. Each update to the blockchain is secured by a cryptographic process known as a *hash function*, which allows the network to immediately detect and reject any attempt to distribute an edited copy of the database.

In this way, blockchains form the foundation for the recording and transfer of fully digital assets. Because the blockchain is always kept in synchronization, there is only ever one true record of ownership — essential to prevent anyone trying to double-spend their assets by sending it to multiple parties at the same time, a problem that plagued previous attempts to create digital assets. Because it is impossible to edit a blockchain once it has been properly updated, parties have mathematically-enforced confidence that the record of their ownership will persist into the future.

---

While the technology is still in early stages, many now believe that if blockchains can create a secure platform for the trade of digital assets, they may also solve the two fundamental challenges facing smart contracts.

**First**, recall that smart contracts require a way for computer code to control real assets. By enabling fully digitized assets, blockchains make it possible for code to exercise control over property. On a blockchain, control over an asset means controlling a cryptographic key that corresponds to the asset in question, rather than any physical object. Thus in our example above, the options contract could *itself* have control of the underlying assets, rather than an escrow agent. When the “exercise” function is called, the operation of the code would transfer the assets without requiring any human assistance.

**Second**, smart contracts need a “trusted computer” that would execute the terms of the contract. This is the blockchain itself. The blockchains that are being developed today are not only databases, but distributed *computers* that can execute code as well as record ownership of assets. Our “smart option” example would itself be uploaded and stored on a blockchain, and would be executed by the blockchain when instructed to do so. The same properties that make blockchains ideal to record ownership of assets also make them ideal for executing smart contracts. Once the code of the contract is uploaded and recorded onto the blockchain, the parties can have confidence that the contract cannot be altered, and that it will always perform as expected.

Blockchain smart contracts may not be as far away as we expect. Banks, exchanges, and other financial institutions are actively developing blockchain technologies that will enable them to store and trade real assets over blockchain systems. Nasdaq, in partnership with blockchain startup Chain, has developed and begun testing a private-market equity trading platform. A next-generation open-source blockchain called Ethereum, launched in July 2015, aims to be the foundation for a new industry of non-traditional decentralized commerce. A consortium of 42 banks, working with blockchain firm R3, have begun work on a shared industry platform based on blockchain technology specifically designed to facilitate financial agreements. Within a few years, financial markets may be trading fully-digital assets across blockchain networks, with the terms of those trades enforced by code.

The impact will not be limited to financial contracts, although these are the most obvious use cases. As techniques are developed that enable other types of property to be recorded and transacted on a blockchain the possible applications for smart contracts will multiply.

---

If they ever become widely used, smart contracts could alter the nature of corporate & commercial transactions. The advantages of software that have revolutionized so many industries — automation, predictability, and speed — could finally be brought to bear on segments of the legal industry.

Representing contractual terms in code, rather than natural language, could bring clarity and predictability to agreements. A smart contract could be tested against any set of inputs — in other words, against any set of material facts which it takes as inputs — allowing lawyers on either side of a deal to know precisely how the contract would execute in every computationally-possible outcome.

In our simple Smart Options example above, each of Alice and Bob could “dry run” the contract in a simulated environment, where every possible input is tested. While this is unnecessary in such a simple example, imagine a contract with thousands of inputs, and hundreds of nested if-then statements — as is common in many complex financial agreements. These, too, could be tested against every possible input defined in the code. Analogous to how software developers “debug” their own code by testing it in every possible circumstance, lawyers could test contracts, giving each side of a deal a clearer understanding of their risk — and perhaps requiring fewer billable hours.

Of course, smart contracts will never fully replace natural-language law. Many types of agreements can never be fully expressed in code or executed by a computer — for instance, those that involve human performance rather than just the exchange of dematerialized assets. Even fully self-executing contracts will ultimately need to make reference to legal terms and concepts that will define each party’s rights if their relationship leads to litigation. Rather, the emergence of smart contracts will lead to a re-evaluation of common practice, as lawyers and clients alike discover which types of agreements and terms are best suited to code, which should be left to natural language, and how to combine each to achieve the best of both worlds.

For now, smart contracts are still speculative fiction. But for the first time we have a technology that could be used to bring them into commercial use. While that day may still be years away, law firms would be wise to consider how these innovations could impact their business. By the time smart contracts become viable, the legal industry should hope that they have lawyers to match.

Subscribe to Josh Stark

Receive the latest updates directly to your inbox.

Verification

This entry has been permanently stored onchain and signed by its creator.

[Arweave Transaction

RmugEXQaZqRVwGb…g8TEhAxrIZ2Nsx4](https://viewblock.io/arweave/tx/RmugEXQaZqRVwGbpX3zU_R9QBw96g8TEhAxrIZ2Nsx4)[Author Address

0x4aa9C5546BE6848…30D25674a1A728e](https://etherscan.io/address/0x4aa9C5546BE68486c4eF264a230D25674a1A728e)

Content Digest

IUqivJ5jeQiCRnw…APpqbBJvyUN0nCg

More from Josh Stark

[View All](https://stark.mirror.xyz/)

###

###

###