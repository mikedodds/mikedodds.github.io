---
title: "Modular reasoning for deterministic parallelism"
collection: publications
category: conferences
permalink: /publication/2011-01-26-modular-reasoning-for-deterministic-parallelism
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2011-01-26
venue: "Principles of Programming Languages (POPL)"
paperurl: "https://mikedodds.github.io/files/publications/2011-01-26-modular-reasoning-for-deterministic-parallelism.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Weaving a concurrency control protocol into a program is difficult and error-prone. One way to alleviate this burden is deterministic parallelism. In this well-studied approach to parallelisation, a sequential program is annotated with sections that can execute concurrently, with automatically injected control constructs used to ensure observable behaviour consistent with the original program.

This paper examines the formal specification and verification of these constructs. Our high-level specification defines the conditions necessary for correct execution; these conditions reflect program dependencies necessary to ensure deterministic behaviour. We connect the high-level specification used by clients of the library with the low-level library implementation, to prove that a client's requirements for determinism are enforced. Significantly, we can reason about program and library correctness without breaking abstraction boundaries.

To achieve this, we use concurrent abstract predicates, based on separation logic, to encapsulate racy behaviour in the library's implementation. To allow generic specifications of libraries that can be instantiated by client programs, we extend the logic with higher-order parameters and quantification. We show that our high-level specification abstracts the details of deterministic parallelism by verifying two different low-level implementations of the library.

DOI: <https://doi.org/10.1145/1926385.1926416>, Paper: [PDF](https://mikedodds.github.io/files/publications/2011-01-26-modular-reasoning-for-deterministic-parallelism.pdf)