# X59YAMLCERT (X59CERT)

The **X59CERT** is a standardized format for certificates that uses the **YAML-encoding** to be human-readable. It provides `sections`, `metadata`, `extensions`, and more to the X59CERT.

The **Standard X59CERT Format** is as follows:

## 

```yaml
---
RequiredInfo:
  - Type: X59CERT
  - Sections: (CodeSigning,Encryption)
  
  - Registar: {SmartContract,DAG,SS,Custom}
  - Revocation: X59Revoke.watch
  - Extensions: {}
CodeSigning:
  - ALGORITHM: {RSA4096,ECDSA,ED25519}

  - pubkey: XX
  - fp: XXXXXXXXXX
Encryption:
  - ALGORITHM: {RSA4096,ECIES_ED25519}

  - pubkey: XX
  - fp: XXXXXXXXXX

```
