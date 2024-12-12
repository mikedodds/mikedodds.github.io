---
title: "Formal Verification of Production Distributed Protocols"
collection: talks
type: "Workshop talk"
permalink: talks/2020-09-15-formal-verification-of-production-distributed-protocols
date: 2020-09-15
venue: "HCSS 2020"
location: "Virtual" 
---

[Slides](https://mikedodds.github.io/files/talks/2020-09-15-formal-verification-of-production-distributed-protocols.pdf), [Talk video](https://sos-vo.org/node/69925)

Byzantine fault-tolerant (BFT) protocols underlie many highly scalable distributed services. For example, distributed databases and blockchain applications both use BFT protocols to ensure that, despite the absence of any central authority, all participants agree on the global state of the database or blockchain. Despite their importance, BFT protocols are notoriously hard to get right because the combination of arbitrary network timing, crashes, and malicious attacks makes for a large number of scenarios to consider.

In this talk we will describe a formal verification methodology suitable for verifying real-world BFT protocols. We will illustrate this methodology with a recent proof of the safety and liveness of the Stellar Consensus Protocol. Working with the Stellar team, we formalized their protocol and identified a previously unknown weakness affecting its liveness properties. Our approach therefore appears to be useful in practice when constructing highly reliable distributed applications that are intended to scale.

Our approach is based on the Ivy verifier developed by McMillan and others. In general, BFT protocols cannot be verified in a push-button manner, but interactive proof is challenging because of the unpredictability of automated solvers. To curb this problem, Ivy restricts the user to proof obligations that fall within a known and well-supported decidable logic. This increases proof-engineer productivity by ensuring that the solver rapidly either confirms the validity of the proof or provides a concrete counter-example.

Ivy can only be applied to systems that can be modelled within its restricted core logic. Surprisingly, we have shown that Ivy is expressive enough to model many intricate distributed protocols, including Stellar. This leads to more rapid verification and proofs that are much more compact than the state-of-the-art.



