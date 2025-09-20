---
title: "Starling: Lightweight Concurrency Verification with Views"
collection: publications
category: conferences
permalink: /publications/2017-07-13-starling-lightweight-concurrency-verification-w-views
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2017-07-13
venue: "Computer Aided Verification (CAV)"
paperurl: "https://mikedodds.github.io/files/publications/2017-07-13-starling-lightweight-concurrency-verification-w-views.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Modern program logics have made it feasible to verify the most complex concurrent algorithms. However, many such logics are complex, and most lack automated tool support. We propose Starling, a new lightweight logic and automated tool for concurrency verification. Starling takes a proof outline written in an abstracted Hoare-logic style, and converts it into proof terms that can be discharged by a sequential solver. Starling’s approach is generic in its structure, making it easy to target different solvers. In this paper we verify shared-variable algorithms using the Z3 SMT solver, and heap-based algorithms using the GRASShopper solver. We have applied our approach to a range of concurrent algorithms, including Rust’s atomic reference counter, the Linux ticketed lock, the CLH queue-lock, and a fine-grained list algorithm.

DOI: <https://doi.org/10.1007/978-3-319-63387-9_27>, Paper: [PDF](https://mikedodds.github.io/files/publications/2017-07-13-starling-lightweight-concurrency-verification-w-views.pdf)

