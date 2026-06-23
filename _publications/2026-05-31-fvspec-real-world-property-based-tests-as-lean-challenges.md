---
title: "FVSpec: Real-World Property-Based Tests as Lean Challenges"
collection: publications
category: preprints
permalink: /publications/2026-05-31-fvspec-real-world-property-based-tests-as-lean-challenges
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2026-05-31
venue: "ArXiv [cs.SE]"
paperurl: "https://arxiv.org/abs/2606.01008"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** We present a benchmark for evaluating AI models and agents on real-world formal software verification tasks. We first scrape 11,039 property-based tests (PBTs) from real-world Python repositories, then automatically translate 2,772 of them (25%) into 9,415 Lean 4 specifications with sorry placeholders (about 3 formalizations/PBT; we retain multiple attempts when none dominates on quality metrics). Translating PBTs into Lean specifications is challenging: it requires modeling Python semantics in Lean, inferring the logical property encoded in an imperative PBT, and handling the inherent difficulties of dependently-typed programming in a seldom-used language. We describe a three-agent LLM pipeline for transpiling PBTs into Lean specifications, evaluate coverage and quality metrics, and provide baselines for proof generation using several automated and model based approaches. All code (scraper and agents) and data (PBTs and Lean specifications) are open source. Our benchmark aims to drive progress on the underexplored problem of AI-assisted formal verification of real-world software, which is of increasing interest as AI produces more and more of the world's code.

DOI: <https://doi.org/10.48550/arXiv.2606.01008>, ArXiv: [Link](https://arxiv.org/abs/2606.01008)
