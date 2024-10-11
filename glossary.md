---
layout: page
title: Glossary
permalink: /glossary/
---

{% for entry in site.glossary %}
- [{{ entry.title }}]({{ entry.url }})
{% endfor %}