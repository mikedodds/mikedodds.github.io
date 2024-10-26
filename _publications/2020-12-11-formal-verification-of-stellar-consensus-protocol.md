---
title: "On the Formal Verification of the Stellar Consensus Protocol"
collection: publications
category: conferences
permalink: /publication/2020-12-11-formal-verification-of-stellar-consensus-protocol
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2020-12-11
venue: "Workshop on Formal Methods for Blockchains (FMBC)"
paperurl: "https://doi.org/10.4230/OASIcs.FMBC.2020.9"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** The Stellar Consensus Protocol (SCP) is a quorum-based BFT consensus protocol. However, instead of using threshold-based quorums, SCP is permissionless and its quorum system emerges from participants’ self-declared trust relationships. In this paper, we describe the methodology we deploy to formally verify the safety and liveness of SCP for arbitrary but fixed configurations. The proof uses a combination of Ivy and Isabelle/HOL. In Ivy, we model SCP in first-order logic, and we verify safety and liveness under eventual synchrony. In Isabelle/HOL, we prove the validity of our first-order encoding with respect to a more direct higher-order model. SCP is currently deployed in the Stellar Network, and we believe this is the first mechanized proof of both safety and liveness, specified in LTL, for a deployed BFT protocol.

DOI: <https://doi.org/10.4230/OASIcs.FMBC.2020.9>, Paper: [PDF](http://mikedodds.github.io/files/publications/2020-12-11-formal-verification-of-stellar-consensus-protocol.pdf)