---
title: "Concurrent Abstract Predicates"
collection: publications
category: conferences
permalink: /publication/2010-06-21-concurrent-abstract-predicates
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2010-06-21
venue: "European Conference on Object-Oriented Programming (ECOOP)"
paperurl: "http://mikedodds.github.io/files/publications/2010-06-21-concurrent-abstract-predicates.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Abstraction is key to understanding and reasoning about large computer systems. Abstraction is simple to achieve if the relevant data structures are disjoint, but rather difficult when they are partially shared, as is often the case for concurrent modules. We present a program logic for reasoning abstractly about data structures that provides a fiction of disjointness and permits compositional reasoning. The internal details of a module are completely hidden from the client by concurrent abstract predicates. We reason about a module’s implementation using separation logic with permissions, and provide abstract specifications for use by client programs using concurrent abstract predicates. We illustrate our abstract reasoning by building two implementations of a lock module on top of hardware instructions, and two implementations of a concurrent set module on top of the lock module.

DOI: <https://doi.org/10.1007/978-3-642-14107-2_24>, Paper: [PDF](http://mikedodds.github.io/files/publications/2010-06-21-concurrent-abstract-predicates.pdf)