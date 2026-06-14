# Reference: How Bitcoin Works

## Overview
Bitcoin is a decentralized digital currency that operates without a central bank or trusted intermediary. The network is maintained by thousands of nodes worldwide, each running the Bitcoin software and enforcing the same rules.

## Case: The Genesis Block
Bitcoin's first block, the genesis block (block 0), was mined by Satoshi Nakamoto on January 3, 2009. It contained a special message: "The Times 03/Jan/2009 Chancellor on brink of second bailout for banks" — a reference to a headline in The Times newspaper. This timestamp serves as proof that the block was created on or after that date. It also makes a statement: Bitcoin was created as an alternative to the fractional-reserve banking system that had just been bailed out.

## Case: The Decentralized Network
There is no central server that "runs" Bitcoin. Every full node validates every transaction and block independently. If a miner produces an invalid block, honest nodes reject it, regardless of how much computing power the miner controls. This is the key insight: decentralization means that no single entity can change the rules. The network consensus is the ultimate authority.

## Case: The Blockchain as Timestamp Server
Satoshi's innovation was combining cryptographic hashing with a timestamp server. Each block contains the hash of the previous block, creating a chain that cannot be altered without re-mining all subsequent blocks. The proof of work required to mine each block makes altering past blocks computationally prohibitive. This is how Bitcoin solves the Byzantine Generals Problem: how to achieve consensus in a network where some participants may be malicious.
