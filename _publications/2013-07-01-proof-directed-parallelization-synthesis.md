---
title: "Proof-Directed Parallelization Synthesis by Separation Logic"
collection: publications
category: manuscripts
permalink: /publication/2013-07-01-proof-directed-parallelization-synthesis
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2013-07-01
venue: "Transactions on Programming Languages and Systems (TOPLAS), Volume 35, Issue 2"
paperurl: "http://mikedodds.github.io/files/publications/2013-07-01-proof-directed-parallelization-synthesis.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** We present an analysis which takes as its input a sequential program, augmented with annotations indicating potential parallelization opportunities, and a sequential proof, written in separation logic, and produces a correctly synchronized parallelized program and proof of that program. Unlike previous work, ours is not a simple independence analysis that admits parallelization only when threads do not interfere; rather, we insert synchronization to preserve dependencies in the sequential program that might be violated by a naïve translation. Separation logic allows us to parallelize fine-grained patterns of resource usage, moving beyond straightforward points-to analysis. The sequential proof need only represent shape properties, meaning we can handle complex algorithms without verifying every aspect of their behavior.

Our analysis works by using the sequential proof to discover dependencies between different parts of the program. It leverages these discovered dependencies to guide the insertion of synchronization primitives into the parallelized program, and to ensure that the resulting parallelized program satisfies the same specification as the original sequential program, and exhibits the same sequential behavior. Our analysis is built using frame inference and abduction, two techniques supported by an increasing number of separation logic tools.

DOI: <https://doi.org/10.1145/2491522.2491525>, Paper: [PDF](http://mikedodds.github.io/files/publications/2016-01-04-proof-directed-parallelization-synthesis.pdf)