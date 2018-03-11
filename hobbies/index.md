---
layout: default
title: "My hobbies"
---

## {{ page.title }}

{% for hobby in site.hobbies %}
* [{{ hobby.title }}](..\{{ hobby.url }})
{% endfor %}
