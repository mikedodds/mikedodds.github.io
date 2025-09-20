---
title: "Compositional Verification of Compiler Optimisations on Relaxed Memory"
collection: publications
category: conferences
permalink: /publications/2018-05-14-compositional-verification-compiler-optimisations
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2018-05-14
venue: "European Symposium on Programming (ESOP)"
paperurl: "https://mikedodds.github.io/files/publications/2018-05-14-compositional-verification-compiler-optimisations.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** A valid compiler optimisation transforms a block in a program without introducing new observable behaviours to the program as a whole. Deciding which optimisations are valid can be difficult, and depends closely on the semantic model of the programming language. Axiomatic relaxed models, such as C++11, present particular challenges for determining validity, because such models allow subtle effects of a block transformation to be observed by the rest of the program. In this paper we present a denotational theory that captures optimisation validity on an axiomatic model corresponding to a fragment of C++11. Our theory allows verifying an optimisation compositionally, by considering only the block it transforms instead of the whole program. Using this property, we realise the theory in the first push-button tool that can verify real-world optimisations under an axiomatic memory model.

DOI: <https://doi.org/10.1007/978-3-319-89884-1_36>, Paper: [PDF](https://mikedodds.github.io/files/publications/2018-05-14-compositional-verification-compiler-optimisations.pdf)

ArXiv version: [Link](https://arxiv.org/abs/1802.05918), ArXiv DOI: <https://doi.org/10.48550/arXiv.1802.05918>