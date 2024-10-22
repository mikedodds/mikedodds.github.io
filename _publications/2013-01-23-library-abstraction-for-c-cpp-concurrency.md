---
title: "Library Abstraction for C/C++ Concurrency"
collection: publications
category: conferences
permalink: /publication/2013-01-23-library-abstraction-for-c-cpp-concurrency
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: XXX
venue: "Principals of Programming Languages (POPL)"
paperurl: "http://mikedodds.github.io/files/publications/2013-01-23-library-abstraction-for-c-cpp-concurrency.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** When constructing complex concurrent systems, abstraction is vi- tal: programmers should be able to reason about concurrent libraries in terms of abstract specifications that hide the implementation details. Relaxed memory models present substantial challenges in this respect, as libraries need not provide sequentially consistent abstractions: to avoid unnecessary synchronisation, they may allow clients to observe relaxed memory effects, and library specifications must capture these.

In this paper, we propose a criterion for sound library abstraction in the new C11 and C++11 memory model, generalising the standard sequentially consistent notion of linearizability. We prove that our criterion soundly captures all client-library interactions, both through call and return values, and through the subtle synchronisation effects arising from the memory model. To illustrate our approach, we verify implementations against specifications for the lock-free Treiber stack and a producer-consumer queue. Ours is the first approach to compositional reasoning for concurrent C11/C++11 programs.

\[DOI: <https://doi.org/10.1145/2429069.2429099>\] \[[PDF](http://mikedodds.github.io/files/publications/2013-01-23-library-abstraction-for-c-cpp-concurrency.pdf)\]