---
title: "Macaw: A Machine Code Toolbox for the Busy Binary Analyst"
collection: publications
category: preprints
permalink: /publications/2024-07-08-macaw-a-machine-code-toolbox
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2024-7-8
venue: "ArXiv [cs.PL]"
paperurl: "https://arxiv.org/abs/2407.06375"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** When attempting to understand the behavior of an executable, a binary analyst can make use of many different techniques. These include program slicing, dynamic instrumentation, binary-level rewriting, symbolic execution, and formal verification, all of which can uncover insights into how a piece of machine code behaves. As a result, there is no one-size-fits-all binary analysis tool, so a binary analysis researcher will often combine several different tools. Sometimes, a researcher will even need to design new tools to study problems that existing frameworks are not well equipped to handle. Designing such tools from complete scratch is rarely time- or cost-effective, however, given the scale and complexity of modern instruction set architectures.

We present Macaw, a modular framework that makes it possible to rapidly build reliable binary analysis tools across a range of use cases. Over a decade of development, we have used Macaw to support an industrial research team in building tools for machine code-related tasks. As such, the name "Macaw" refers not just to the framework itself, but also a suite of tools that are built on top of the framework. We describe Macaw in depth and describe the different static and dynamic analyses that it performs, many of which are powered by an SMT-based symbolic execution engine. We put a particular focus on interoperability between machine code and higher-level languages, including binary lifting from x86 to LLVM, as well verifying the correctness of mixed C and assembly code.

DOI: <https://doi.org/10.48550/arXiv.2407.06375>