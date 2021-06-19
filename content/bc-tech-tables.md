
|Chain|Encoding lib|DSA (Digital Signature Algo)|
|---|---|---|
|Polkadot|Scale|Edwardscurve (Ed25519 / EdDSA)|
|Cardano|cbor|Ellipticcurve (Secp256k1? / EcDSA)|
|Near|borch|Ellipticcurve|
|Bitcoin|asn.1?|Ellipticcurve|

### Encoding

|Name|More|JS, TS|C#|Java|
|---|---|---|---|---|
|Scale|https://substrate.dev/docs/en/knowledgebase/advanced/codec||||

[Polkadot DSAa](https://wiki.polkadot.network/docs/en/build-protocol-info#cryptography)  
[More](https://substrate.dev/docs/en/knowledgebase/advanced/cryptography)

* Ed25519
* Sr25519 - Schnorr signatures on the Ristretto group
* ECDSA signatures on secp256k1

[Polkadot address prefixes](https://wiki.polkadot.network/docs/en/build-protocol-info#addresses)

Polkadot: 0
Kusama: 2
Westend: 42


Done