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
* __Ph.D__ Biostatistics, Western University
* __M.MATH__ Applied Mathematics, University of Waterloo, 2016
* __B.Sc__ Applied Mathematics, Western University, 2014 

Techincal Skills
======
* Python (Frequently used libraries: sklearn, numpy, scipy, pandas)
* R (Frequently used libraires: caret, glmnet, tidyr, dplyr)
* SQL (Postgres and SQLite)
* MATLAB
* Some SAS

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  

