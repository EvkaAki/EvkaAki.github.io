---
layout: default
title: "School projects"
---
## {{ page.title }} :school_satchel:
{% assign name = (site.projects | where: "language","laravel") %}
During my studies, I had to make various projects, from witch some of them are listed bellow. Despite the fact, that two of this projects ({% for p in name %}{% if forloop.index == 1 %} {{ p.subject }}, {% else %}{{ p.subject }}{% endif %}{% endfor %}) will be implemented in the php framework laravel I'm fully new to web development and therefore have no experience in this field.
{% for p in site.projects %}
* [{{ p.start_date | date_to_string }} {{p.subject}} {{ p.title }}](..\{{ p.url }}.html)
{% endfor %}
