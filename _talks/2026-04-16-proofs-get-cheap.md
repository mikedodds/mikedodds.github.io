---
title: "What Happens to Software When Proof is Cheap?"
collection: talks
type: "Distinguished Lecture"
permalink: /talks/2026-04-16-proofs-get-cheap
date: 2026-04-16
venue: "UW Allen School Distinguished Lecture Series 2025/26"
location: "Seattle, WA"
---

[Slides](https://mikedodds.github.io/files/talks/2026-04-16-proofs-get-cheap.pdf), [Talk video](https://www.youtube.com/watch?v=oSHVPvM56sA)

In July 2025, three AI systems independently achieved gold-medal standard at the International Math Olympiad. One of them, Harmonic's Aristotle, did it by constructing formal proofs in the Lean proof assistant. Six months later, several AIs working together used Lean to solve an open problem posed by Paul Erdős. We may soon live in a strange world where AI is better at math than any human expert.

Lean and tools like it bridge two worlds: mathematicians use them to formalise theorems, but engineers use them to prove that code behaves correctly. This second use, formal verification, has a long history and a few notable successes in cryptography, operating systems, and parser security. But these successes have always been limited by the sheer difficulty of the mathematical reasoning they require.

Now, AI may be changing this picture. If mathematical reasoning is cheap, we could eliminate entire classes of bugs from systems at scale, guarantee that safety-critical code behaves as intended, or verify auto-generated code as fast as it is written. Our need for rigorous verification is growing just as the cost of doing so may be dropping.

The most important software in need of verification may be AI systems themselves. These are growing more capable and more opaque, and we are granting them increasing power over consequential decisions. The same advances making mathematical proof cheaper may also be creating the systems that most urgently need to be proved safe.
