---
title: "Crux, a Precise Verifier for Rust and Other Languages"
collection: publications
category: preprints
permalink: /publications/2024-10-23-crux-a-precise-verifier-for-rust
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2024-10-23
venue: "ArXiv [cs.PL]"
paperurl: "https://arxiv.org/abs/2410.18280"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:**  We present Crux, a cross-language verification tool for Rust and C/LLVM. Crux targets bounded, intricate pieces of code that are difficult for humans to get right: for example, cryptographic modules and serializer / deserializer pairs. Crux builds on the same framework as the mature SAW-Cryptol toolchain, but Crux provides an interface where proofs are phrased as symbolic unit tests. Crux is designed for use in production environments, and has already seen use in industry.

In this paper, we focus on Crux-MIR, our verification tool for Rust. Crux-MIR provides a bit-precise model of safe and unsafe Rust which can be used to check both inline properties about Rust code, and extensional equality to executable specifications written in Cryptol or in the hacspec dialect of Rust. Notably, Crux-MIR supports compositional reasoning, which is necessary to scale to even moderately complex proofs. We demonstrate Crux-MIR by verifying the Ring library implementations of SHA1 and SHA2 against pre-existing functional specifications.

Crux is available at <https://crux.galois.com>.

DOI: <https://doi.org/10.48550/arXiv.2410.18280>