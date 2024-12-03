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
* Ph.D., Computer Science, University of York, 2009
* M.Sc., Computer Systems and Software Engineering, University of York, 2004 

Work experience
======
* Galois, Inc, Principal Scientist, 2017 - Present
  * Leads research projects in safety and security critical domains, with a particular focus on static analysis in industry, logic-based verification, concurrency verification, and software/hardware reasoning, 

* University of York, Anniversary Lecturer, 2012 - 2017
  * Conducted research-focused lectureship—roughly equivalent to an Associate Professor in the United States (see the Awards section below).

* University of Cambridge, Research Associate, 2008 - 2012
  * Worked on EPSRC-funded research projects under Dr. M. Parkinson and Prof. P. Sewell. 
  
Grants 
======

* DARPA PROVERS / VERSE - usable formal methods for engineers (current)
* DARPA LiLaC-SL / ALLSTAR - C2Rust extension project (current) 
* DARPA CAMDEN - incentive design for government procurement processes 
* DARPA PEARLS / REVERSER - AI-driven formal methods tools 
* DARPA BARC - automated binary lifting and compartmentalization 
* DARPA SafeDocs / SPARTA - safe parser technologies 

Awards 
======

* Facebook Secure the Internet grant, 2018. Research grant: “Verified C++ Cryptography with SAW and Cryptol”. 
* Microsoft Research PhD Scholarship, 2016. Fully-funded PhD scholarship, “Lightweight concurrency modeling”.
* Royal Society Industry fellowship, 2015. Permanent membership of the Royal Society college of Industry Fellows, and two years of funding to collaborate with Microsoft Research Cambridge.
* London Mathematical Society grant, 2014. Collaboration grant, “A theory of correctness for weakly-ordered algorithms.”
* York Anniversary Research Lectureship, 2012. Twenty such lectureships were created at the University of York in 2012, awarded competitively across all subjects.


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
