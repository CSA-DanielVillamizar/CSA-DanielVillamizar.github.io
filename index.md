---
title: Instrucciones alojadas en línea
permalink: index.html
layout: home
---

# Content Directory

Hipervínculos a cada uno de los tutoriales. 

## Tutoriales

{% assign wts = site.pages | where_exp:"page", "page.url contains '/Instructions/Walkthroughs'" %}
| Module | Walkthrough |
| --- | --- | 
{% for activity in wts %}| {{ activity.wts.module }} | [{{ activity.wts.title }}{% if activity.wts.type %} - {{ activity.wts.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

