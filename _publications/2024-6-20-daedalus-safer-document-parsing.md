---
title: "Daedalus: Safer Document Parsing"
collection: publications
category: conferences
permalink: /publication/2024-6-20-daedalus-safer-document-parsing
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2024-6-20
venue: "Programming Language Design and Implementation (PLDI) 2024"
paperurl: "https://doi.org/10.1145/3656410"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** Despite decades of contributions to the theoretical foundations of parsing and the many tools available to aid in parser development, many security attacks in the wild still exploit parsers. The issues are myriad—flaws in memory management in contexts lacking memory safety, flaws in syntactic or semantic validation of input, and misinterpretation of hundred-page-plus standards documents. It remains challenging to build and maintain parsers for common, mature data formats. In response to these challenges, we present Daedalus, a new domain-specific language (DSL) and toolchain for writing safe parsers. Daedalus is built around functional-style parser combinators, which suit the rich data dependencies often found in complex data formats. It adds domain-specific constructs for stream manipulation, allowing the natural expression of parsing noncontiguous formats. Balancing between expressivity and domain-specific constructs lends Daedalus specifications simplicity and leaves them amenable to analysis. As a stand-alone DSL, Daedalus is able to generate safe parsers in multiple languages, currently C++ and Haskell. We have implemented 20 data formats with Daedalus, including two large, complex formats—PDF and NITF—and our evaluation shows that Daedalus parsers are concise and performant. Our experience with PDF forms our largest case study. We worked with the PDF Association to build a reference implementation, which was subject to a red-teaming exercise along with a number of other PDF parsers and was the only parser to be found free of defects.

\[DOI: <https://doi.org/10.1145/3656410>\] \[[PDF](http://mikedodds.github.io/files/publications/2024-6-20-daedalus-safer-document-parsing.pdf)\]