
|Chain|Encoding lib|DSA (Digital Signature Algo)|Address format|
|---|---|---|---|
|Bitcoin|asn.1?|EcDSA|Base58Check|
|Cardano|cbor|EcDSA?||
|Ethereum|?|EcDSA||
|Near|Borsh|EcDSA||
|Polkadot|Scale|EdDSA|SS58|

### Serializers / Encoders

|Name|More|JS, TS|C#|Java|Rust|
|---|---|---|---|---|---|
|Asn.1|||[.Net5](https://docs.microsoft.com/en-us/dotnet/api/system.formats.asn1?view=net-5.0)|||
|[Borsh](https://borsh.io)||[borsh-js](https://github.com/near/borsh-js)||[borshj](https://github.com/near/borshj)|[borsh-rs](https://github.com/near/borsh-rs)|
|Cbor|||[.Net5](https://docs.com/en-us/dotnet/api/system.formats.cbor?view=dotnet-plat-ext-5.0)|||
|[Scale](https://substrate.dev/docs/en/knowledgebase/advanced/codec)|||[polkadot_api_dotnet](https://github.com/usetech-llc/polkadot_api_dotnet/blob/master/Polkadot/src/Utils/Scale.cs)|||

### [Public-Key](https://en.wikipedia.org/wiki/Public-key_cryptography) Signature schemes / Digital Signature Algos

|Curve|Name|Abbrev|JS, TS|C#|Java|Rust|
|---|---|---|---|---|---|---|
|[secp256k1](https://en.bitcoin.it/wiki/Secp256k1)|Elicptic Curve|[EcDSA](https://en.bitcoin.it/wiki/Elliptic_Curve_Digital_Signature_Algorithm)||[.Net5](https://docs.microsoft.com/en-us/dotnet/api/system.security.cryptography.ecdsa.create?view=net-5.0)|||
|Ed25519|Edwards curve|EdDSA||||[wasm-crypto](https://github.com/polkadot-js/wasm/blob/master/packages/wasm-crypto/src/rs/ed25519.rs)|
|Sr25519|Schnorr||[schnorrkel-js](https://github.com/polkadot-js/schnorrkel-js)|||[wasm-crypto](https://github.com/polkadot-js/wasm/blob/master/packages/wasm-crypto/src/rs/sr25519.rs)|

#### DOT

[Polkadot DSAs](https://wiki.polkadot.network/docs/en/build-protocol-info#cryptography)  
[More](https://substrate.dev/docs/en/knowledgebase/advanced/cryptography)

* Ed25519
* Sr25519 - Schnorr signatures on the Ristretto group
* ECDSA signatures on secp256k1

### Address Formats

|Name|More|JS, TS|C#|Java|
|---|---|---|---|---|
|Base58Check|||||
|[SS58](https://substrate.dev/docs/en/knowledgebase/advanced/ss58-address-format)||[polkadot-js](https://github.com/polkadot-js/ss58)|[polkadot_api_dotnet](https://github.com/usetech-llc/polkadot_api_dotnet/blob/master/Polkadot/src/Utils/Address.cs)||

### Address Prefixes

#### DOT

[Polkadot address prefixes](https://wiki.polkadot.network/docs/en/build-protocol-info#addresses)

Polkadot: 0
Kusama: 2
Westend: 42


Done