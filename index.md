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

## Core facts

- Addresses are Q1 bech32m, written with a capital Q.
- The asset is QTOV. Its base unit is the Quon, where one QTOV is one million Quon. The testnet asset is TQTOV.
- The gateway is an HTTP POST to `/v1/<method>` with a flat JSON body. See the [gateway reference](/developers/docs/apis/gateway/).
- The client SDK is the QCore family. QCore.rs is the Rust core, QCore.js is published on npm as `@qunatovainc/qcore`, and QCore.py is the Python binding.
- The fungible token standard is [QAsset](/developers/docs/standards/qasset/). The non fungible standard is [QCollectible](/developers/docs/standards/qcollectible/).
- The name service is [QNS](/developers/docs/qns/), with domains under a capital Q top level domain such as Jeff.Q.

## Where to go next

- New to the cryptography, start with [post quantum cryptography](/developers/docs/post-quantum-cryptography/).
- Building an app, see [smart contracts](/developers/docs/smart-contracts/) and the [APIs](/developers/docs/apis/).
- Running infrastructure, see [nodes and clients](/developers/docs/nodes-and-clients/).
