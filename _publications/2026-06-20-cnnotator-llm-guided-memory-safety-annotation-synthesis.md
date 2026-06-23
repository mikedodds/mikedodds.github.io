---
title: "CNnotator: LLM-Guided Memory Safety Annotation Synthesis"
collection: publications
category: conferences
permalink: /publications/2026-06-20-cnnotator-llm-guided-memory-safety-annotation-synthesis
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2026-06-20
venue: "Workshop on Code Translation, Transformation, and Modernization (ReCode), co-located with ICSE"
paperurl: "https://doi.org/10.1145/3786180.3788313"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Memory safety errors account for a large proportion of security bugs in systems written in C; modern languages such as Java and Rust prevent such bugs because they are memory-safe by design. To migrate systems to safer languages or identify memory errors, we must first determine how legacy code manipulates memory. This information is only represented implicitly in such code. In many cases, memory usage patterns are merely tedious for humans to figure out, rather than truly difficult. In this work, we ask if large language models (LLMs) can perform this task by having them synthesize annotations representing memory usage as specifications in CN, a hybrid testing/verification tool. Our tool, CNnotator, uses LLMs to automatically generate and test CN specifications. We find that current models are able to generate CN specifications for small-to-medium C programs, with the OpenAI o3 reasoning model achieving a 90% success rate on first attempts and 97% overall success, while the chat model GPT-4o correctly annotates 65% of first attempts. These results suggest AI-assisted annotation is becoming practical for real-world C codebases.

DOI: <https://doi.org/10.1145/3786180.3788313>, ArXiv: [Link](https://arxiv.org/abs/2606.21822), Paper: [PDF](https://mikedodds.github.io/files/publications/2026-06-20-cnnotator-llm-guided-memory-safety-annotation-synthesis.pdf)
