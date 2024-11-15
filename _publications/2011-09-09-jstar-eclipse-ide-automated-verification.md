---
title: "jStar-eclipse: an IDE for automated verification of Java programs"
collection: publications
category: conferences
permalink: /publication/2011-09-09-jstar-eclipse-ide-automated-verification
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2011-09-09
venue: "Principles and practice of parallel programming (PPoPP)"
paperurl: "http://mikedodds.github.io/files/publications/2011-09-09-jstar-eclipse-ide-automated-verification.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** jStar is a tool for automatically verifying Java programs. It uses separation logic to support abstract reasoning about object specifications. jStar can verify a number of challenging design patterns, including Subject/Observer, Visitor, Factory and Pooling. However, to use jStar one has to deal with a family of command-line tools that expect specifications in separate files and diagnose the errors by inspecting the text output from these tools.

In this paper we present a plug-in, called jStar-eclipse, allowing programmers to use jStar from within Eclipse IDE. Our plug-in allows writing method contracts in Java source files in form of Java annotations. It automatically translates Java annotations into jStar specifications and propagates errors reported by jStar back to Eclipse, pinpointing the errors to the locations in source files. This way the plug-in ensures an overall better user experience when working with jStar. Our end goal is to make automated verification based on separation logic accessible to a broader audience.

DOI: <https://doi.org/10.1145/2025113.2025182>, Paper: [PDF](http://mikedodds.github.io/files/publications/2011-09-09-jstar-eclipse-ide-automated-verification.pdf)