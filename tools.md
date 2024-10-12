---
layout: page
title: Tools
permalink: /tools/
---

{% assign sections = "" | split: '' %}
{% for tool in site.tools %}
    {% if tool.section %}
    {% assign section = tool.section %}
    {% unless sections contains section %}
        {% assign sections = sections | push: section %}
    {% endunless %}
    {% endif %}
{% endfor %}

{% assign sections = sections | sort %}

{% for section in sections %}
## {{ section }}
{% for tool in site.tools %}
{% if tool.section == section %}
- [{{ tool.title }}]({{ site.baseurl }}{{ tool.url }})
{% endif %}
{% endfor %}
{% endfor %}


