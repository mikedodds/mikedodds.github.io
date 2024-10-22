---
title: "Verified Cryptographic Code for Everybody"
collection: publications
category: conferences
permalink: /publication/2021-07-15-verified-cryptographic-code-for-everybody
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2021-7-15
venue: "Computer Aided Verification (CAV)"
paperurl: "http://mikedodds.github.io/files/publications/2021-07-15-verified-cryptographic-code-for-everybody.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** We have completed machine-assisted proofs of two highly- optimized cryptographic primitives, AES-256-GCM and SHA-384. We have verified that the implementations of these primitives, written in a mix of C and x86 assembly, are memory safe and functionally correct, by which we mean input-output equivalent to their algorithmic specifications. Our proofs were completed using SAW, a bounded cryptographic verification tool which we have extended to handle embedded x86. The code we have verified comes from AWS LibCrypto. This code is identical to BoringSSL and very similar to OpenSSL, from which it ultimately derives. We believe we are the first to formally verify these implementations, which protect the security of nearly everybody on the internet.
