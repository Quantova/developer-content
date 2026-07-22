---
title: Introduction to Quantova
description: A high level introduction to Quantova, a sovereign post quantum Layer 1 built from scratch.
lang: en
---

# Introduction to Quantova

Quantova is a sovereign post quantum Layer 1 built from scratch. Every account, transaction, and container is secured with NIST standardized post quantum cryptography. There is no elliptic curve and no classical public key cryptography anywhere in the chain, so nothing in the trust base is vulnerable to Shor. Quantova is at the testnet and pre audit stage and external audits are still ahead.

## Why Quantova exists

Bitcoin, Ethereum, and Solana all depend on cryptography that a sufficiently capable quantum computer can break. This is an infrastructure problem rather than a distant research problem, and it cannot be patched onto a live chain after the fact. Networks that will secure long lived value need to be post quantum before that value moves on chain.

## What makes it different

- Post quantum from genesis. Signatures use ML-DSA-65 from FIPS 204, key exchange uses ML-KEM-768 from FIPS 203, and SLH-DSA from FIPS 205 is available as a hash based signature. Hashing uses SHA-3 and SHAKE from FIPS 202, and the transport channel uses ChaCha20-Poly1305. This cryptography is our own from scratch build called Q-Crypto.
- QORUS consensus. QORUS is a committee byzantine fault tolerant protocol. A budget bounded committee is drawn by sortition each round, and finality is committed with ML-DSA-65 authority keys. See [QORUS consensus](/developers/docs/qorus-consensus/).
- The QVM. The [Quantova Virtual Machine](/developers/docs/qvm/) is a register machine that runs compiled containers. It is not the Ethereum virtual machine and it is not wasm.
- The Quanta language. Contracts are written in [Quanta](/developers/docs/smart-contracts/quanta/), a language where whole exploit classes fail to compile.
