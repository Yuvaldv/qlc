---
title: Technical Overview
weight: 2
pre: ""
---
## What is a Blockchain?
The blockchain is a distributed ledger technology allowing for secure and transparent Peer-to-Peer trust with regards to financial currencies & assets as well as legal agreements, contracts, signatures, terms & conditions.

## What are Blocks?
A block is a locked & unmodifiable collection of valid transaction records which is sealed by a timestamp of its creation and chained to the previous block. You may think of them as individual pages of a ledger.

## How are they Chained?
Each block hold's a cryptographic-hash of the previous block thus chaining them together. this is somewhat similar to the hash protocol used in Bit-Torrent.

## How is that secure?
By effectively creating [Byzantine Fault Tolerance](https://medium.com/loom-network/understanding-blockchain-fundamentals-part-1-byzantine-fault-tolerance-245f46fe8419) blockchain technologies have ubiquitously created a safe protocol for every use case, given enough scale.

There are three parameters for the blockchain's security, one is it's **decentralization** the other is each block's timestamped **seal** and the third is **the chain** itself.

**Distributed & Decentralized** - The blockchain is partially or entirely replicated, held and cross-referenced across every one of its miners called peers. thus if I as a hacker wanted to change a record within a block, I would have to do it **simultaneously** across the all the peers which hold that block.

**The Chain** - Since each block contains the hash of the previous block I, as a hacker, would have to start with the first block and hack my way towards the target block through the entire blockchain and different peers holding them.

**The Seal** - Any modification to the block will change it's timestamped seal. Thus, I, as a hacker, would have to change all the seals, or cryptographic-hash-codes- of every block after my block to correlate with the changes I've made.

So, to put it simply, while a small and relatively centralized blockchain might be somewhat penetrable, and while tools that interact with the blockchain such as wallets, might be vulnerable, A blockchain with enough peers is virtually impenetrable.

## How is it different from a cryptocurrency?
While reading through articles concerning crypto and blockchain you may find that these terms are used interchangeably for the most part and even synonymously for some publications the difference between them is important. While the blockchain is a ledger holding transaction records of assets, cryptocurrencies are but an asset that exists on these blockchains. [Read More.](https://techcrunch.com/2018/07/22/the-blockchain-begins-finding-its-way-in-the-enterprise/)

The following difference is also imperative to understand, while there can be several blockchains running on different platform providers such as Quorum, IBM Blockchain, or [Raiden](https://raiden.network/) since all of these platforms make use of [Ethereum open-source blockchain technology](https://github.com/ethereum/), all the blockchains that use these platforms as their infrastructure will use Ethereum's protocol.

## Is there one single Blockchain?
While someday there may exist a single global blockchain holding all asset types, or more likely interfaces connecting different blockchains, today there are many independent blockchains generally holding a single, or several closely related assets. Each coin has it's own blockchain and there are various, some open-source, architectures to the blockchain technology such as [NEM](https://nem.io/) or [HyperLedger](https://www.hyperledger.org/).

## Are there different types of blockchain?
Yes, there certainly are. There are three manners to differentiate blockchains, each with their own set of archetypes
### Transparency & Permission

**Public Blockchains** allow anyone to participate (mine) for the blockchain and the transaction records are completely transparent.

**Private Blockchains** publish only partial transaction details if any.

**Permissionless Blockchains** allow anyone to mine the blockchain, i.e write transaction details to a block.

**Permissioned Blockchains** only allow certain users to write transactions or even specific transaction details,

a *public permissioned* blockchain is often referred to as Consortium or Federated blockchain

[Read More](https://hackernoon.com/3-popular-types-of-blockchains-you-need-to-know-7a5b98ee545a)

### By the underlying infrastructure
Just like web development where your tech-stack i.e the programming language and frameworks you use affect how your product behaves and how you maintain it. The same applies to the blockchain, whether you use [NEM](https://github.com/NemProject), [Ethereum](https://github.com/ethereum/), [Bitcoin](https://github.com/bitcoin/bitcoin) or [Hyperledger](https://github.com/hyperledger) to create your blockchain makes a big difference in how you're solution will handle certain types of interactions.

####  By the different Consensus Protocols - Proof-of-X
Relating to the previous point, certain types of blockchains use different consensus protocols to chain a new block.

#### PoW  (Bitcoin, Ethereum, LiteCoin)
Proof-of-Work requires a miner whose attempting to chain a new block of transactions to solve a highly complex and CPU intensive puzzle while competing with other users for who'll come first and mine the block and reap some coin.

This method is criticized for requiring a vast amount of electricity and CPU power.

#### PoS  (Ethereum, NXT, PeerCoin, DeCred)
Proof-of-Stake uses a miners' stake on the coin $$ Stake = \frac{Users' Coins}{All Coins}$$, to help decide who gets to mine it. Generally by an automated voting system.

Proof of Stake is often is used together with proof-of-work by capping a user to mining the transactions amount relative to their stake in the coin.

a Delegated proof of stake allows to group several miners together under one user, and compound their the stake of the coin.

This method would mean that miners need to retain a large amount of coin instead of cashing it for profits in order to grow their mining capacity

#### PoI  (NEM)
Proof-of-Importance adds on Proof of Stake the variable of the age of your currency, and how long you've held it, as well as the number of transactions you made, not only mined.

[Read More](https://nem.io/xem/harvesting-and-poi/)

#### Proof of Space (Chia, SpaceMint, BurstCoin)
Sometimes referred to as proof of capacity, proof of space requires a proof that the miner has reserved and designated sufficient amount of RAM and HDD/SSD storage space to handle the transaction, this is done by solving a low-CPU, high storage capacity riddle.
This method mainly aims to solve the electricity consumption of mining cryptocurrencies.

New consensus protocols are still emerging so keep on eye on the best fit for your solution.
