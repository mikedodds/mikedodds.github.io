---
title: "A simple abstraction for complex concurrent indexes"
collection: publications
category: conferences
permalink: /publications/2011-10-22-simple-abstraction-complex-concurrent-datastructures
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2011-10-22
venue: "Object oriented Programming Systems Languages and Applications (OOPSLA)"
paperurl: "https://mikedodds.github.io/files/publications/2011-10-22-simple-abstraction-complex-concurrent-datastructures.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Indexes are ubiquitous. Examples include associative arrays, dictionaries, maps and hashes used in applications such as databases, file systems and dynamic languages. Abstractly, a sequential index can be viewed as a partial function from keys to values. Values can be queried by their keys, and the index can be mutated by adding or removing mappings. Whilst appealingly simple, this abstract specification is insufficient for reasoning about indexes accessed concurrently. We present an abstract specification for concurrent indexes. We verify several representative concurrent client applications using our specification, demonstrating that clients can reason abstractly without having to consider specific underlying implementations. Our specification would, however, mean nothing if it were not satisfied by standard implementations of concurrent indexes. We verify that our specification is satisfied by algorithms based on linked lists, hash tables and B-Link trees. The complexity of these algorithms, in particular the B-Link tree algorithm, can be completely hidden from the client's view by our abstract specification.

DOI: <https://doi.org/10.1145/2048066.2048131>, Paper: [PDF](https://mikedodds.github.io/files/publications/2011-10-22-simple-abstraction-complex-concurrent-datastructures.pdf)