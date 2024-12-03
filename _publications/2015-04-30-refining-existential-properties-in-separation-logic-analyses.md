---
title: "Refining Existential Properties in Separation Logic Analyses"
collection: publications
category: preprints
permalink: /publications/2015-04-30-refining-existential-properties-in-separation-logic-analyses
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2015-04-30
venue: "ArXiv [cs.LO]"
paperurl: "https://doi.org/10.48550/arXiv.1504.08309"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** In separation logic program analyses, tractability is generally achieved by restricting invariants to a finite abstract domain. As this domain cannot vary, loss of information can cause failure even when verification is possible in the underlying logic. In this paper, we propose a CEGAR-like method for detecting spurious failures and avoiding them by refining the abstract domain. Our approach is geared towards discovering existential properties, e.g. "list contains value x". To diagnose failures, we use abduction, a technique for inferring command preconditions. Our method works backwards from an error, identifying necessary information lost by abstraction, and refining the forward analysis to avoid the error. We define domains for several classes of existential properties, and show their effectiveness on case studies adapted from Redis, Azureus and FreeRTOS.

DOI: <https://doi.org/10.48550/arXiv.1504.08309>