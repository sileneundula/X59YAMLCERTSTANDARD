# 1. The Standard Decentralized X59 Registar Ledger

The **Decentralized X59 Registar (DX59Reg)** is a **novel creation** detailing the methodology of creating standard **X59 Certificates** and a **Decentralized Public-Key Infrastructure (D-PKI)**. Its approach is a decentralized way of verifying certificate details such as encryption public key and signatures. It has many advances over the RFC5280 system implemented for certificate authorities, making certificates more modern.

## Purpose

This document serves as a standard to these certificates and approaches to decentralization of the ecosystem. It aims to make certificates modern and addresses many issues found in current Public-Key Infrastructures (PKIs). As a standard, it aims to make it modular to build off of and adds more functionality.

## Approaches To `DX59Reg`

* Block Lattice / DAG
* Substrate
* Raft and Libp2p
* Smart Contracts

## Cryptographic Primitives

- Verifiable Random Functions (VRF)
- Zero-Knowledge Proofs

## Method 1: Raft Protocol

The consensus protocol **Raft** is used to verify the integrity of the certificate. A RocksDB storage is used to store certificates and Raft is implemented to verify certificates. To verify encryption public keys, a chain of randomness is created using a verifable random function (VRF). It derives the randomness from the public key and seed. This request is then used to prove the encryption key is valid by creating a random value derived from the public key that is then decrypted by the certificate. This is then verified by all nodes in the Raft and if valid, all nodes have to agree. An **Authority Signature** is provided when all nodes agree. This authority signature can take many forms, such as:

- Aggregated BLS Signatures
- Single Trusted Authority
- Multi-Signature
- Ring Signature

## Method 2: Block Lattice (DAG) For `DX59Registar`

The novel method of using a **dual ledger (blockchain/block lattice system)** for certificate registration is the current focus. It offers many advantages offer prior attempts at certficates. It provides high-value integrity to the certificates by storing them in a blockchain, or more specifically block lattice, to allow decentralized approaches to management of certificates. It can offer smart contract functionality and extensions.
