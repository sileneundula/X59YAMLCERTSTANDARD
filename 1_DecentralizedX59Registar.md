# 1. The Standard Decentralized X59 Registar Ledger

The **Decentralized X59 Registar (DX59Reg)** is a **novel creation** detailing the methodology of creating standard **X59 Certificates**. Its approach is a decentralized way of verifying certificate details such as encryption public key and signatures. It has many advances over the RFC5280 system implemented for certificate authorities, making certificates more modern.

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
