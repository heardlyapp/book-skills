# Reference: Wallets & Security

## Overview
A Bitcoin wallet manages your keys. The security of your Bitcoin depends entirely on how you manage your private keys. There is no "forgot password" option in Bitcoin.

## Case: Cold Storage vs Hot Wallets
Cold storage means keeping private keys on a device that has never been connected to the internet. Hardware wallets (Ledger, Trezor, Coldcard) are the most common form. Hot wallets (mobile apps, browser extensions) are connected to the internet and convenient for daily use but vulnerable to remote attacks. The general rule: keep long-term savings in cold storage, and only keep small amounts in hot wallets for spending.

## Case: Seed Phrases and BIP39
A seed phrase (mnemonic) is a set of 12 or 24 words that encodes the entropy from which all keys in an HD wallet are derived. The seed phrase is the ultimate backup: anyone who has your seed phrase has your Bitcoin, regardless of whether they have your PIN, your hardware wallet, or your password. Seed phrases should be stored on paper (or engraved metal) in a secure physical location. Never store a seed phrase digitally — no screenshots, no cloud storage, no encrypted files.

## Case: Multisignature Wallets
A multisig wallet requires M-of-N signatures to spend funds. For example, a 2-of-3 wallet requires 2 out of 3 authorized key holders to sign any transaction. This provides redundancy (if one key is lost, funds can still be spent) and security (an attacker would need to compromise more than one key). Multisig is the standard for large Bitcoin holdings, corporate treasuries, and custody services.
