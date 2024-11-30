---
title: "Trustworthy Runtime Verification via Bisimulation (Experience Report)"
collection: publications
category: conferences
permalink: /publications/2023-08-31-trustworthy-runtime-verification
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2023-08-31
venue: "International Conference on Functional Programming (ICFP)"
paperurl: "https://doi.org/10.1145/3607841"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** When runtime verification is used to monitor safety-critical systems, it is essential that monitoring code behaves correctly. The Copilot runtime verification framework pursues this goal by automatically generating C monitor programs from a high-level DSL embedded in Haskell. In safety-critical domains, every piece of deployed code must be accompanied by an assurance argument that is convincing to human auditors. However, it is difficult for auditors to determine with confidence that a compiled monitor cannot crash and implements the behavior required by the Copilot semantics.

In this paper we describe CopilotVerifier, which runs alongside the Copilot compiler, generating a proof of correctness for the compiled output. The proof establishes that a given Copilot monitor and its compiled form produce equivalent outputs on equivalent inputs, and that they either crash in identical circumstances or cannot crash. The proof takes the form of a bisimulation broken down into a set of verification conditions. We leverage two pieces of SMT-backed technology: the Crucible symbolic execution library for LLVM and the What4 solver interface library. Our results demonstrate that dramatically increased compiler assurance can be achieved at moderate cost by building on existing tools. This paves the way to our ultimate goal of generating formal assurance arguments that are convincing to human auditors.

DOI: <https://doi.org/10.1145/3607841>, Paper: [PDF](https://mikedodds.github.io/files/publications/2023-08-31-trustworthy-runtime-verification.pdf)