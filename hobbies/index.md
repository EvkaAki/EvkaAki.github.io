---
layout: default
title: "My hobbies"
---

## {{ page.title }} :heart:

{% for hobby in site.hobbies %}
* [{{ hobby.title }}]({{ hobby.url }}.html) {{ hobby.logo }}
{% endfor %}
