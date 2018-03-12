---
layout: default
title: "School projects"
---
## {{ page.title }} :school_satchel:
{% assign p = site.projects | where: "language","laravel" %}
During my studies, I had to make various projects, from witch some of them are listed bellow. Despite the fact, that two of this projects ({% for p in p %}{% if  forloop.rindex == 0 %} {{ p.subject }} {% else %}{{ p.subject }}, {% endif %}{% endfor %}) will be implemented in the php framework laravel I'm fully new to web development and therefore have no experience in this field.
{% for p in site.projects %}
* [{{ p.start_date | date: "%Y" }} - _{{p.subject}}_ : **{{ p.title }}**](\{{ p.url }}.html)
{% endfor %}
