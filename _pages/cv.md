---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D., Computer Science, [University of York](https://www.cs.york.ac.uk), 2009 (supervisor: D. Plump)
* M.Sc., Computer Systems and Software Engineering, [University of York](https://www.cs.york.ac.uk), 2004 

Work experience
======
* [Galois, Inc.](https://galois.com), Principal Scientist, 2017 - Present
  * Leads research projects in safety- and security-critical domains, with a particular focus on static analysis in industry, logic-based verification, concurrency verification, and software/hardware reasoning. Galois is a research company whose tools are used by NASA, AWS, and the US Department of Defense.

* [University of York](https://www.cs.york.ac.uk), Anniversary Research Lecturer, 2012 - 2017
  * Conducted a research-focused lectureship—roughly equivalent to an Associate Professor in the United States (see the Awards section below).

* [University of Cambridge](https://www.cst.cam.ac.uk), Research Associate, 2008 - 2012
  * Worked on EPSRC-funded research projects with Dr. M. Parkinson and Prof. P. Sewell.

Scientific leadership
======

Scientific lead on multiple research programs and commercial engagements in formal verification, security, and AI-driven reasoning:

* **Verified cryptographic systems** (AWS). Led formal verification of core components of Amazon's s2n-TLS and [AWS-LibCrypto](https://github.com/awslabs/aws-lc-verification) libraries—among the first deployments of formally verified cryptography in production at scale—using [SAW](https://saw.galois.com), Galois's cryptographic verification tool.
* **Verification tooling** (Apple). Led Galois's work building [Isabelle support for SAW](https://www.galois.com/articles/announcing-isabelle-support-for-saw) to support [Apple's formal verification of corecrypto](https://security.apple.com/blog/formal-verification-corecrypto/).
* **AI benchmarking** (UK ARIA). Led development of [FV-Spec](https://fvspec.galois.com/), an AI benchmark for the UK Advanced Research and Invention Agency, consisting of 5,000+ formal verification challenge problems synthesised from real-world use cases.
* **Usable verification tools** ([DARPA PROVERS](https://www.darpa.mil/research/programs/pipelined-reasoning-of-verifiers-enabling-robust-systems)). Led an 8-organisation industry-academic collaboration building formal verification tools for national security applications. Hardened and scaled [CN](https://rems-project.github.io/cn-tutorial/), a verification tool for C, with the University of Cambridge.
* **C-to-Rust translation** ([DARPA TRACTOR](https://www.darpa.mil/program/translating-all-c-to-rust)/ALLSTAR). Led Galois's work translating C codebases to secure idiomatic Rust, extending Galois's [c2rust](https://c2rust.com) transpiler to AI-driven translation workflows.
* **AI-driven formal methods** ([DARPA PEARLS](https://www.darpa.mil/research/programs/proof-engineering-adaptation-repair-and-learning-for-software)). Led development of early AI-driven formal verification tools, including a reinforcement-learning proof synthesiser for SAW.
* **Safe parsing** ([DARPA SafeDocs](https://www.darpa.mil/research/programs/safe-documents)). Led development of [Daedalus](https://galoisinc.github.io/daedalus/), a language for building secure data parsers, highlighted by DARPA as a high-priority tool in their formal verification research spotlight.

Awards and honours
======

* **Royal Society Industry Fellowship**, 2015. Permanent membership of the Royal Society college of Industry Fellows, and two years of funding to collaborate with Microsoft Research Cambridge.
* **York Anniversary Research Lectureship**, 2012. Twenty such lectureships were created at the University of York in 2012, awarded competitively across all subjects.
* **Imperial College Junior Research Fellowship**, 2012. Ranked first among Engineering faculty applicants (declined in favour of the York lectureship).
* **Facebook Secure the Internet grant**, 2018. Research grant: “Verified C++ Cryptography with SAW and Cryptol”.
* **Microsoft Research PhD Scholarship**, 2016. Fully-funded PhD scholarship: “Lightweight concurrency modeling”.
* **London Mathematical Society grant**, 2014. Collaboration grant: “A theory of correctness for weakly-ordered algorithms.”

Selected writing
======

* [Specifications Don't Exist](https://galois.com/articles/specifications-dont-exist) (2025). Argues that specification, not proof, is the bottleneck for scalable formal verification.
* [Claude Can (Sometimes) Prove It](https://galois.com/articles/claude-can-sometimes-prove-it) (2025). Evaluates frontier AI models on real formal verification tasks.
* [o3, Frontier Math, and the Future of Mathematics](https://galois.com/articles/o3-frontier-math-and-the-future-of-mathematics/) (2025). Analyses the implications of AI mathematical reasoning for formal methods.
* [Formally Verifying Industry Cryptography](https://doi.org/10.1109/MSEC.2022.3153035), IEEE Security & Privacy (2022). Describes Galois's approach to deploying formal verification in production cryptographic systems.

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
