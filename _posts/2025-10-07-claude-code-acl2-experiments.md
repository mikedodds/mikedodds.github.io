---
title: 'Experimenting with ACL2 and Claude Code'
date: 2025-10-07
permalink: /posts/2025/10/claude-code-acl2-experiments
tags:
  - ai
  - formal-methods
  - interactive-theorem-proving
---

**TL;DR:** Using only prompting with Claude Code, I created:
- [50+ ACL2 theorem proofs](https://github.com/septract/acl2-swf-experiments) translated from [Software Foundations](https://softwarefoundations.cis.upenn.edu/)
- [An MCP server for ACL2](https://github.com/septract/acl2-mcp) with stateful solver sessions

Total time: ~3-4 hours. I wrote zero lines of code by hand.

---

AI models are getting more powerful, but most training data is in high-representation languages like Python. That's a potential issue for formal methods, where most languages have lower representation in training corpora. I'd [already experimented with Lean](https://www.galois.com/articles/claude-can-sometimes-prove-it) and gotten interesting results, but after a discussion with some colleagues about lower-representation ITPs, I got curious about [ACL2](https://www.cs.utexas.edu/users/moore/acl2/). It's lower-representation compared to Lean, with quite a different idiomatic way of doing proof, and I'd never used it before.

I played around with Claude Code for a few hours and got [50+ theorems to go through](https://github.com/septract/acl2-swf-experiments), progressing from basic arithmetic properties through induction, list operations, and finally polymorphic higher-order functions. The examples were lifted from [Software Foundations](https://softwarefoundations.cis.upenn.edu/) book 1, selected and translated by Claude Code through prompting alone.

If you want to play with ACL2 yourself, you might find the [CLAUDE.md](https://github.com/septract/acl2-swf-experiments/blob/main/CLAUDE.md) and [notes/acl2-quick-reference.md](https://github.com/septract/acl2-swf-experiments/blob/main/notes/acl2-quick-reference.md) files useful (also written by Claude based on reading web resources).

## Building an MCP Server for ACL2

As I worked on more complex proofs, I realized Claude Code would benefit from better tooling for iterative theorem development. So I had it build [an MCP server for ACL2](https://github.com/septract/acl2-mcp) in Python—again, entirely through prompting. The server provides 15 different tools for interacting with ACL2, but the key sophistication is persistent session management with checkpoint/rollback support. This lets you save your prover state before attempting risky proof steps, then roll back if they don't work out. I built this in a couple of phases:

1. I asked Claude Code to make a beta
2. I used it with Claude Code in a separate session to write ACL2 proofs, and asked Claude Code for feedback on missing features
3. I told Claude Code to fix the feedback

I also asked Claude Code for security audits at two points, which resulted in a lot of extra input validation. It's still unsafe really just because ACL2 isn't containerized. That'd be reasonably easy to do but feels like overkill for this experiment.

## What This Means

The fact that Claude Code could handle ACL2—a language it has relatively little training data for, with quite different idioms from Lean—suggests that representation gap might matter less than we'd expect for current frontier models. At least for introductory-level theorems, the models seem able to pick up the syntax and proof patterns through in-context learning.

Of course, this was mostly straightforward material from an introductory textbook. The harder question is whether these techniques scale to research-level mathematics or industrial verification. But it's encouraging to find that the barrier to entry is now "spend a few hours prompting" rather than "spend weeks learning a new proof assistant."

The most interesting moment was watching Claude Code struggle with the `fold-product-append` theorem. When I asked it to reflect on the experience afterward, here's what it said:

> "This was genuinely challenging—it's not just about finding the right lemmas, but understanding how ACL2's rewriter works under the hood. The theorem proves that `fold-product (append l1 l2) = (fold-product l1) * (fold-product l2)`, which requires showing that multiplication can be rearranged across nested structures. The key insight was that ACL2's commutativity rules were being too aggressive, normalizing terms before the arithmetic reasoning could apply. The solution required selective theory control: globally disabling `commutativity-of-*` during the main induction, then re-enabling both commutativity and associativity at the specific subgoal (Subgoal *1/3'') where they're needed. This demonstrates something interesting about interactive theorem proving—sometimes the prover knows the facts it needs, but you have to carefully orchestrate when those facts are applied. The proof failed with multiple simpler strategies (direct hints, helper lemmas, manual instantiation) before this approach worked."

I think that's a pretty interesting reflection on what makes proof engineering tricky.
