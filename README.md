# LNP/BP Specifications

LNP/BP stands for "Bitcoin Protocol / Lightning Network Protocol". This set of specifications covers standards & best
practices for Layer 2, 3 solutions (and above) in cases when they do not require soft- or hard-forks on the Bitcoin
blockchain level and are not directly related to issues covered in Lightning Network RFCs (BOLTs).

Basically, LNP/BPs cover everything that can be anchored to Bitcoin transactions, defines primitives for L2+ solution
design and describes complex use cases which can be built from some primitives. This allows such solutions as financial
assets, storage, messaging, computing and different forms of secondary markets leveraging Bitcoin security model and
Bitcoin as a method of payment/medium of exchange.

Criteria for a LNP/BP specification proposal:
* Should not be covered by existing or proposed BIPs
* Should not cause soft- or hard-fork in Bitcoin blockchain (but may depend on soft-forks from an existing BIP proposals)
* Should not distort Bitcoin miner's economic incentives
* Should not pollute Bitcoin blockchain with unnecessary non-transaction related data or have to maintain such pollution
  as low as possible
* Should not be covered by existing or proposed BOLTs
* Must not require a utility or security tokens to function (but may enable creation of digital assets or tokenized
physical goods)
* Must not depend on non-bitcoin blockchains (but may be applicable to bitcoin-compatible blockchains)


## List of current LNP/BP proposals

No | Layer | Vertical | Title | Author(s) | Type | Status
------:| ----- | -------- | ----- | ----- | ---- | ------
[1](lnpbp-0001.md) | Transaction (1) | Bitcoin protocol | Key tweaking: collision-resistant elliptic curve-based commitments | Maxim Orlovsky et al | Standard | Final
[2](lnpbp-0002.md) | Transaction (1) | Bitcoin protocol | Deterministic embedding of cryptographic ommitments into transaction output scriptPubkey | Maxim Orlovsky et al | Standard | Proposal
[3](lnpbp-0003.md) | Transaction (1) | Bitcoin protocol | Deterministic definition of transaction output containing cryptographic commitment | Giacomo Zucco et al | Standard | Proposal
[4](lnpbp-0004.md) | Client-validated data (3) | Cryptographic primitives | Multi-message commitment scheme with zero-knowledge provable unique properties | Maxim Orlovsky | Standard | Proposal
[5](lnpbp-0005.md) | Transaction graph (2) | Bitcoin protocol | Universal short Bitcoin identifiers for blocks, transactions and their inputs & outputs | Christian Decker et al | Standard | Proposal
6 | Transaction (1) | Bitcoin protocol | Deterministic bitcoin commitments | Maxim Orlovsky | Standard | Draft
7 | Client-validated data (3) | Consensus layer | Strict encoding | Peter Todd, Maxim Orlovsky | Standard | Planned
[8](https://petertodd.org/2016/commitments-and-single-use-seals) | Client-validated data (3) | Cryptographic primitives | Single-use-seals | Peter Todd, Maxim Orlovsky | Informational | Draft
[9](https://diyhpl.us/wiki/transcripts/scalingbitcoin/milan/client-side-validation/) | Client-validated data (3) | Consensus layer | Client-side validation | Peter Todd, Maxim Orlovsky | Informational | Draft
[10](lnpbp-0010.md) | Transaction graph (2) | Bitcoin protocol | Bitcoin transaction output-based single-use-seals | Peter Todd et al | Standard | Proposal
[11](lnpbp-0011.md) | Client-validated graphs (4) | Smart contracts | RGB: Client-validated confidential smart contracts using bitcoin transaction graphs for Bitcoin and Lightning Network | Maxim Orlovsky et al | Informational | Proposal
12 | Client-validated graphs (4) | Consensus layer | RGB Schema: client-side validation rules for RGB smart contracts | Maxim Orlovsky | Standard | Planned
13 | Client-validated graphs (4) | Consensus layer | RGB client-side verification and data structures | Maxim Orlovsky | Standard | Planned
14 | Client-validated data (3) | Smart contracts | Bech32 encoding of RGB data | Maxim Orlovsky | Standard | Planned
[15](lnpbp-0015.md) | OSI Session (i5) | Lightning network protocol | LNP handshake and encryption in network communications based on Noise_XK (BOLT-8 extract) | Multiple peers | Standard | Proposal
16 | OSI Session (i5) | Lightning network protocol | LNP handshake over WebSockets | Maxim Orlovsky | Standard | Planned
17 | OSI Session (i5) | Lightning network protocol | LNP handshake over ZMQ sockets | Maxim Orlovsky | Standard | Planned
[18](lnpbp-0018.md) | OSI Transport (i4) | Lightning network protocol | LNP native message framing protocol (BOLT-8 extract) | Multiple peers | Standard | Planned
[19](lnpbp-0019.md) | OSI Presentation (i6) | Lightning network protocol | LNP P2P remote procedure call protocol (BOLT-1 & BOLT-9 extracts) | Multiple peers | Standard | Planned
[20](lnpbp-0020.md) | Application (5) | Smart contracts | RGB fungible assets schema (RGB-20) | Multiple peers | Standard | Final
[21](lnpbp-0021.md) | Application (5) | Smart contracts | RGB non-fungible assets schema for collectibles (RGB-21) | Multiple peers | Standard | Proposal
[22](https://github.com/LNP-BP/LNPBPs/issues/29) | Application (5) | Smart contracts | RGB reputation and identity schema (RGB-22) | Multiple peers | Standard | Draft
23 | Application (5) | Smart contracts | RGB verifiably-unique history log for audited data (RGB-23) | Multiple peers | Standard | Planned
[30](https://github.com/pandoracore/prometheus-spec) | Transaction graph (2) | State channels | Prometheus: trustless multiparty computing with escrow & arbitration | Maxim Orlovsky | Standard | Draft
[31](https://github.com/storm-org/storm-spec) | Transaction graph (2) | State channels | Storm: trustless storage with escrow contracts | Maxim Orlovsky | Standard | Draft
[32](https://github.com/pandoracore/ibiss-spec) | Client-validated data (3) | Game theory | Incentive-based interactive settlement scheme for computation integrity arguments | Maxim Orlovsky, Sabina Sachtachtinskagia | Informational | Draft
33 | Application (5) | Smart contracts | Spectrum: routed RGB state swaps over Lightning Network | Multiple peers | Standard | Planned
34 | OSI Application (i7) | Smart contracts | RGB P2P wire protocol | Maxim Orlovsky | Standard | Planned
35 | OSI Application (i7) | Lightning network protocol | Bitforst: P2P data storage & backup protocol | Maxim Orlovsky | Standard | Planned
[36](https://github.com/LNP-BP/LNPBPs/issues/21) | OSI Presentation (i6) | API | Recommendations for API design | Maxim Orlovsky | Informational | Draft
[37](https://github.com/LNP-BP/LNPBPs/pull/23/files) | Application (5) | Smart contracts | Invoicing formats for RGB-20 fungible assets schema | Alekos Filini | Standard | Draft

### Invited or planned proposals to join LNP/BP standards family

1. Discreet log contracts: deterministic transaction structure, embedding into lightning network, wire protocols
    - [Specification effort](https://github.com/discreetlogcontracts/dlcspecs)
    - [Lightning Discreet Log Contract Channels](https://hackmd.io/@lpQxZaCeTG6OJZI3awxQPQ/LN-DLC)
2. Different [pre-Schnorr schemes for scriptless scripts](https://lists.linuxfoundation.org/pipermail/lightning-dev/2019-November/002316.html)
3. Generalized lightning network standartisation and related [eltoo](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2018-April/015907.html) and [PTLC](https://suredbits.com/payment-points-part-2-stuckless-payments/) proposals
4. Micropayments:
    - [Lightspeed micropayments for Lightning Network](https://github.com/LNP-BP/LNPBPs/issues/24) by Maxim Orlovsky
    - [LSAT Authentication and Payments for the Lightning-Native Web](https://lightning.engineering/posts/2020-03-30-lsat/) by Olaoluwa Osuntokun


## Layers for LNP/BP proposals:

No | Title | Description | Examples
------------------:| ----- | ----------- | ---------
1                  | Transaction | Data or protocols defined for a single bitcoin transaction (both off-chain and on-chain) | Cryptographic primitives, advanced multisignature schemes, transaction structure
2                  | Transaction graph | Data and protocols defined on a transaction graph | State channels, sidechains
3                  | Client-validated data | Protocols and formats for off-chain data (persistent or ephemeral) | Cryptographic primitives, serialization
4                  | Client-validated graphs | Protocols and formats for off-chain graph structures | Complex commitment schemes, schemata
5                  | Application | Specific high-level applications build of underlying layers | Assets, audit, storage, computing, messaging, decentralized exchanges and marketplaces

Additionally to these layers there is a set of network protocol layers organized according to [ISO OSI model](https://en.wikipedia.org/wiki/OSI_model#Layer_architecture), with numbers prefixed using `i` symbol ("complex dimension").
