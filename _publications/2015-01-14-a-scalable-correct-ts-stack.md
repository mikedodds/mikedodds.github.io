---
title: "A Scalable, Correct Time-Stamped Stack"
collection: publications
category: conferences
permalink: /publication/2015-01-14-a-scalable-correct-ts-stack
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2015-01-14
venue: "Principles of Programming Languages (POPL)"
paperurl: "http://mikedodds.github.io/files/publications/2015-01-14-a-scalable-correct-ts-stack.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Concurrent data-structures, such as stacks, queues, and deques, often implicitly enforce a total order over elements in their underlying memory layout. However, much of this order is unnecessary: linearizability only requires that elements are ordered if the insert methods ran in sequence. We propose a new approach which uses timestamping to avoid unnecessary ordering. Pairs of elements can be left unordered if their associated insert operations ran concurrently, and order imposed as necessary at the eventual removal.

We realise our approach in a new non-blocking data-structure, the TS (timestamped) stack. Using the same approach, we can define corresponding queue and deque data-structures. In experiments on x86, the TS stack outperforms and outscales all its competitors -- for example, it outperforms the elimination-backoff stack by factor of two. In our approach, more concurrency translates into less ordering, giving less-contended removal and thus higher performance and scalability. Despite this, the TS stack is linearizable with respect to stack semantics.

The weak internal ordering in the TS stack presents a challenge when establishing linearizability: standard techniques such as linearization points work well when there exists a total internal order. We present a new stack theorem, mechanised in Isabelle, which characterises the orderings sufficient to establish stack semantics. By applying our stack theorem, we show that the TS stack is indeed linearizable. Our theorem constitutes a new, generic proof technique for concurrent stacks, and it paves the way for future weakly ordered data-structure designs.

DOI: <https://doi.org/10.1145/2676726.2676963>, Paper: [PDF](http://mikedodds.github.io/files/publications/2015-01-14-a-scalable-correct-ts-stack.pdf)
