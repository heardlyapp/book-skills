# Reference: Transactions & Script

## Overview
Bitcoin transactions are not simple "send X to address Y." They are programs written in Bitcoin Script that unlock and create UTXOs. Understanding transaction structure is essential for anyone building on Bitcoin.

## Case: The UTXO Model
Unlike a bank account balance, Bitcoin uses the UTXO model. Your "balance" is the sum of all unspent transaction outputs (UTXOs) controlled by your keys. When you send Bitcoin, you consume one or more UTXOs as inputs and create new UTXOs as outputs. Any excess amount becomes "change" returned to a new address in your wallet. This model enables privacy (different addresses for each transaction) and parallelism (multiple inputs can be combined).

## Case: Bitcoin Script
Bitcoin transactions are validated by executing scripts. The most common script is P2PKH (Pay to Public Key Hash), which requires the recipient to provide a public key that hashes to the specified address and a valid digital signature. More complex scripts enable multisignature (require M-of-N signatures), time locks (funds cannot be spent before a certain block height), and hash locks (used in Lightning Network).

## Case: Transaction Fees
Transaction fees are the difference between the total value of inputs and outputs. Miners prioritize transactions with higher fee rates (satoshis per byte). When there is more demand for block space than capacity (1-4 MB per block), fees increase. This is the fee market that ensures transactions are eventually confirmed even when the network is congested.
