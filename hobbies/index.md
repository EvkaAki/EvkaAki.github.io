---
layout: default
title: "My hobbies"
---

## {{ page.title }} :heart:

{% for hobby in site.hobbies %}
* [{{ hobby.title }}](..\{{ hobby.url }}) {{ hobby.logo }}
{% endfor %}
