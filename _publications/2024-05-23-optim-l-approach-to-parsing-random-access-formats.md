---
title: "Research Report: An Optim (l) Approach to Parsing Random-Access Formats"
collection: publications
category: conferences
permalink: /publication/2024-05-23-optim-l-approach-to-parsing-random-access-formats
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2024-05-23
venue: "Tenth LangSec Workshop at IEEE Security & Privacy"
paperurl: "http://mikedodds.github.io/files/publications/2024-05-23-optim-l-approach-to-parsing-random-access-formats.pdf"
---

**Abstract:** We introduce a Domain Specific Language (DSL) that allows for the declarative specification of random access formats (formats that include offsets or require out of order parsing, e.g., zip, ICC, and PDF). Our DSL is composed by layering three distinct computational languages: first, we have the base layer of primitive parsers (these could use various “off the shelf” parsing technology). Second, upon this base we layer our XRP (eXplicit Region Parser) DSL, a pure functional language for declaratively specifying random-access formats. XRP, although similar to parser combinators, gives greater control and expressiveness by making parsing regions explicit. Third, we embed XRP into Optim (l), a novel DSL that describes Directed Acyclic Graphs (DAGs) of computations. A node represents a computation in XRP, an edge represents a dependency between the computations. From a declarative Optim (l) program we can generate an imperative module that provides an API for ondemand and incremental parsing of the random access format.

DOI: <https://doi.org/10.1109/SPW63631.2024.00023>, LangSec workshop link: [here](https://langsec.org/spw24/abstracts.html#rr1), Paper: [PDF](http://mikedodds.github.io/files/publications/2024-05-23-optim-l-approach-to-parsing-random-access-formats.pdf), Slides: [PDF](http://mikedodds.github.io/files/talks/2024-05-23-SLIDES-optim-l-approach-to-parsing-random-access-formats.pdf)