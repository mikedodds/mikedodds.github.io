---
title: "Safe asynchronous multicore memory operations"
collection: publications
category: conferences
permalink: /publication/2011-11-06-safe-asynchronous-multicore-memory-operations
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2011-11-06
venue: "Automated Software Engineering (ASE)"
paperurl: "http://mikedodds.github.io/files/publications/2011-11-06-safe-asynchronous-multicore-memory-operations.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Asynchronous memory operations provide a means for coping with the memory wall problem in multicore processors, and are available in many platforms and languages, e.g., the Cell Broadband Engine, CUDA and OpenCL. Reasoning about the correct usage of such operations involves complex analysis of memory accesses to check for races. We present a method and tool for proving memory-safety and race-freedom of multicore programs that use asynchronous memory operations. Our approach uses separation logic with permissions, and our tool automates this method, targeting a C-like core language. We describe our solutions to several challenges that arose in the course of this research. These include: syntactic reasoning about permissions and arrays, integration of numerical abstract domains, and utilization of an SMT solver. We demonstrate the feasibility of our approach experimentally by checking absence of DMA races on a set of programs drawn from the IBM Cell SDK.

DOI: <https://doi.org/10.1109/ASE.2011.6100049>, Paper: [PDF](http://mikedodds.github.io/files/publications/2011-11-06-safe-asynchronous-multicore-memory-operations.pdf)