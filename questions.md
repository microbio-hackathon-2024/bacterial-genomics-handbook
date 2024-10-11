---
layout: page
title: Frequently Asked Questions
permalink: /questions/
---

## Before Starting

{% for question in site.questions %}
  {% if question.step == "before_starting" %}
- [{{ question.title }}]({{ site.baseurl }}{{ question.url }})
  {% endif %}
{% endfor %}


## Data Preparation

{% for question in site.questions %}
  {% if question.step == "data_preparation" %}
- [{{ question.title }}]({{ site.baseurl }}{{ question.url }})
  {% endif %}
{% endfor %}

## Quality Control

{% for question in site.questions %}
  {% if question.step == "qc" %}
- [{{ question.title }}]({{ site.baseurl }}{{ question.url }})
  {% endif %}
{% endfor %}

## Analysis

{% for question in site.questions %}
  {% if question.step == "analysis" %}
- [{{ question.title }}]({{ site.baseurl }}{{ question.url }})
  {% endif %}
{% endfor %}

## Results

{% for question in site.questions %}
  {% if question.step == "results" %}
- [{{ question.title }}]({{ site.baseurl }}{{ question.url }})
  {% endif %}
{% endfor %}
