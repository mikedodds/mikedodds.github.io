---
title: "Verifying Custom Synchronization Constructs Using Higher-Order Separation Logic"
collection: publications
category: manuscripts
permalink: /publication/2016-01-04-verifying-custom-synchronization-constructs
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2016-01-04
venue: "Transactions on Programming Languages and Systems (TOPLAS), Volume 38, Issue 2"
paperurl: "http://mikedodds.github.io/files/publications/2016-01-04-verifying-custom-synchronization-constructs.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Synchronization constructs lie at the heart of any reliable concurrent program. Many such constructs are standard (e.g., locks, queues, stacks, and hash-tables). However, many concurrent applications require custom synchronization constructs with special-purpose behavior. These constructs present a significant challenge for verification. Like standard constructs, they rely on subtle racy behavior, but unlike standard constructs, they may not have well-understood abstract interfaces. As they are custom built, such constructs are also far more likely to be unreliable.

This article examines the formal specification and verification of custom synchronization constructs. Our target is a library of channels used in automated parallelization to enforce sequential behavior between program statements. Our high-level specification captures the conditions necessary for correct execution; these conditions reflect program dependencies necessary to ensure sequential behavior. We connect the high-level specification with the low-level library implementation to prove that a client’s requirements are satisfied. Significantly, we can reason about program and library correctness without breaking abstraction boundaries.

To achieve this, we use a program logic called iCAP (impredicative Concurrent Abstract Predicates) based on separation logic. iCAP supports both high-level abstraction and low-level reasoning about races. We use this to show that our high-level channel specification abstracts three different, increasingly complex low-level implementations of the library. iCAP’s support for higher-order reasoning lets us prove that sequential dependencies are respected, while iCAP’s next-generation semantic model lets us avoid ugly problems with cyclic dependencies.

DOI: <https://doi.org/10.1145/2818638>, Paper: [PDF](http://mikedodds.github.io/files/publications/2016-01-04-verifying-custom-synchronization-constructs.pdf)