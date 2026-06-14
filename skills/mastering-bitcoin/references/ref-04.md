# Reference: Mining & Consensus

## Overview
Mining is the process by which new Bitcoin blocks are created. It serves three purposes: issuing new Bitcoin, securing the network through proof of work, and achieving decentralized consensus.

## Case: Proof of Work Algorithm
Miners construct a block header containing the previous block's hash, the Merkle root of transactions, a timestamp, and a nonce. They hash this header with SHA256 twice until the result is below the current target difficulty. The target adjusts every 2016 blocks so that blocks are found approximately every 10 minutes. As of 2024, the Bitcoin network computes approximately 500 exahashes per second (500 quintillion hashes per second). No other network has this much security.

## Case: Mining Pools
Individual miners rarely find blocks. Mining pools aggregate the computing power of thousands of miners and distribute rewards proportionally. The largest pools control significant percentages of the network's hash rate. While pools are technically centralized, miners can switch pools instantly if one becomes too large, which prevents any single pool from gaining permanent control.

## Case: The Halving
The block reward started at 50 BTC in 2009 and halves every 210,000 blocks (~4 years). The most recent halving (2024) reduced the reward to 3.125 BTC. This decaying issuance schedule ensures that the total supply of Bitcoin will never exceed 21 million. The last Bitcoin will be mined around the year 2140. After that, miners will be compensated entirely through transaction fees.
