---
layout: page
title: Glossary
permalink: /glossary/
---

{% assign letters = "" | split: '' %}
{% for entry in site.glossary %}
    {% assign letter = entry.title | upper | slice 0, 0 %}
    {% unless letters contains letter %}
        {% assign letters = letters | push: letter %}
    {% endunless %}
{% endfor %}

{% assign letters = letters | sort %}

{% for letter in letters %}
## {{ letter }}

{% for entry in site.glossary %}
{% assign x = entry.title | upper | slice 0, 0 %}

{% if x == letter %}
- [{{ entry.title }}]({{ entry.url }})
{% endif %}
{% endfor %}

{% endfor %}

