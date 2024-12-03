---
title: "Proving Linearizability Using Partial Orders"
collection: publications
category: conferences
permalink: /publications/2017-03-19-proving-linearizability-using-partial-orders
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2017-03-19
venue: "European Symposium on Programming (ESOP)"
paperurl: "https://arxiv.org/abs/1701.05463"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Linearizability is the commonly accepted notion of correctness for concurrent data structures. It requires that any execution of the data structure is justified by a linearization --- a linear order on operations satisfying the data structure's sequential specification. Proving linearizability is often challenging because an operation's position in the linearization order may depend on future operations. This makes it very difficult to incrementally construct the linearization in a proof.

We propose a new proof method that can handle data structures with such future-dependent linearizations. Our key idea is to incrementally construct not a single linear order of operations, but a partial order that describes multiple linearizations satisfying the sequential specification. This allows decisions about the ordering of operations to be delayed, mirroring the behaviour of data structure implementations. We formalise our method as a program logic based on rely-guarantee reasoning, and demonstrate its effectiveness by verifying several challenging data structures: the Herlihy-Wing queue, the TS queue and the Optimistic set.

Conference paper DOI: <https://doi.org/10.1007/978-3-662-54434-1_24>

ArXiv version of the paper: [Link](https://arxiv.org/abs/1701.05463), ArXiv paper DOI: <https://doi.org/10.48550/arXiv.1701.05463>