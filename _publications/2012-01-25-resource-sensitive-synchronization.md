---
title: "Resource-sensitive synchronization inference by abduction"
collection: publications
category: conferences
permalink: /publications/2012-01-25-resource-sensitive-synchronization
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2012-01-25
venue: "Principles of Programming Languages (POPL)"
paperurl: "https://mikedodds.github.io/files/publications/2012-01-25-resource-sensitive-synchronization.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** We present an analysis which takes as its input a sequential program, augmented with annotations indicating potential parallelization opportunities, and a sequential proof, written in separation logic, and produces a correctly-synchronized parallelized program and proof of that program. Unlike previous work, ours is not an independence analysis; we insert synchronization constructs to preserve relevant dependencies found in the sequential program that may otherwise be violated by a naive translation. Separation logic allows us to parallelize fine-grained patterns of resource-usage, moving beyond straightforward points-to analysis. Our analysis works by using the sequential proof to discover dependencies between different parts of the program. It leverages these discovered dependencies to guide the insertion of synchronization primitives into the parallelized program, and to ensure that the resulting parallelized program satisfies the same specification as the original sequential program, and exhibits the same sequential behaviour. Our analysis is built using frame inference and abduction, two techniques supported by an increasing number of separation logic tools.

DOI: <https://doi.org/10.1145/2103656.2103694>, Paper: [PDF](https://mikedodds.github.io/files/publications/2012-01-25-resource-sensitive-synchronization.pdf)