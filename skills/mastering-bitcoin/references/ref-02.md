# Reference: Cryptography & Keys

## Overview
Bitcoin uses public-key cryptography to secure ownership. Users control their Bitcoin through cryptographic keys, not accounts or passwords. Understanding key management is essential to using Bitcoin safely.

## Case: Elliptic Curve Cryptography
Bitcoin uses the secp256k1 elliptic curve standard to generate key pairs. A private key is simply a random 256-bit number. The corresponding public key is derived through elliptic curve multiplication — a one-way function that is computationally infeasible to reverse. This means anyone can derive a public key from a private key, but no one can derive a private key from a public key (without solving the discrete logarithm problem).

## Case: Hierarchical Deterministic Wallets
BIP32 (Bitcoin Improvement Proposal 32) introduced hierarchical deterministic wallets. Instead of generating random keys, an HD wallet derives all keys from a single seed phrase (usually 12 or 24 words). The seed phrase can generate a tree of keys, allowing wallet software to manage billions of addresses from a single mnemonic. This is a massive improvement over early "random key" wallets, where each key had to be backed up individually.

## Case: Addresses and Payment Requests
A Bitcoin address is derived from a public key through two rounds of hashing (SHA256 followed by RIPEMD160) with a checksum. Addresses are typically encoded in Base58Check (a base-58 encoding with error detection) to prevent typing errors. Bitcoin addresses starting with "1" are legacy P2PKH addresses. Those starting with "bc1" are native SegWit addresses (Bech32).
