---
title: "Deny-Guarantee Reasoning"
collection: publications
category: conferences
permalink: /publication/2009-03-22-deny-guarantee-reasoning
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2009-03-22
venue: "European Symposium on Programming (ESOP)"
paperurl: "https://mikedodds.github.io/files/publications/2009-03-22-deny-guarantee-reasoning.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Rely-guarantee is a well-established approach to reasoning about concurrent programs that use parallel composition. However, parallel composition is not how concurrency is structured in real systems. Instead, threads are started by ‘fork’ and collected with ‘join’ commands. This style of concurrency cannot be reasoned about using rely-guarantee, as the life-time of a thread can be scoped dynamically. With parallel composition the scope is static.

In this paper, we introduce deny-guarantee reasoning, a reformulation of rely-guarantee that enables reasoning about dynamically scoped concurrency. We build on ideas from separation logic to allow interference to be dynamically split and recombined, in a similar way that separation logic splits and joins heaps. To allow this splitting, we use deny and guarantee permissions: a deny permission specifies that the environment cannot do an action, and guarantee permission allow us to do an action. We illustrate the use of our proof system with examples, and show that it can encode all the original rely-guarantee proofs. We also present the semantics and soundness of the deny-guarantee method.

DOI: <https://doi.org/10.1007/978-3-642-00590-9_26>, Paper: [PDF](https://mikedodds.github.io/files/publications/2009-03-22-deny-guarantee-reasoning.pdf)