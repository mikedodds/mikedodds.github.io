---
title: "PhD Thesis: Graph Transformation and Pointer Structures"
collection: publications
category: misc
permalink: /publication/2008-09-01-phd-thesis-mike-dodds
# excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2008-09-01
venue: "University of York, Department of Computer Science"
paperurl: "https://mikedodds.github.io/files/publications/2008-09-01-phd-thesis-mike-dodds.pdf"
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

**Abstract:** This thesis is concerned with the use of graph-transformation rules to specify and manipulate pointer structures. In it, we show that graph transformation can form the basis of a practical and well-formalised approach to specifying pointer properties. We also show that graph transformation rules can be used as an efficient mechanism for checking the properties of graphs.

We make context-sensitive graph transformation rules more practical for specifying structures, by improving their worst-case application time. We define syntactic conditions ensuring faster application of rules, and we show how these conditions improve the application time of sequences of rules. We apply these fast graph transformation systems to the problem of recognising graph languages in linear time, and show that several interesting context-sensitive languages can be recognised using this approach.

We examine the relationship between pointer specification using context-free graph transformation and separation logic, an alternative approach to reasoning about pointers. We show that formulas in a fragment of separation logic can be translated into a restricted class of hyperedge replacement grammars, and vice versa, showing that these two approaches are of equivalent power. This means that our fragment inherits the formal properties of hyperedge-replacement grammars, such as inexpressibility results. We show that several operators of full separation logic cannot be expressed using hyperedge replacement.

We define a C-like language that uses graph transformation rules to ensure pointer safety. This language includes graph transformation constructs for defining and rewriting pointer structures. These constructs can be statically checked for shape safety by modelling them as graph transformation rules. We give both an abstract graph-transformation semantics and a concrete executable semantics for our new constructs, and prove that the semantics correspond.

Thesis: [PDF](https://mikedodds.github.io/files/publications/2008-09-01-phd-thesis-mike-dodds.pdf)