---
layout: page
title: Questions
permalink: /questions/
---

## Before Starting

{% for question in site.questions %}
  {% if question.step == "before_starting" %}
- [{{ question.title }}]({{ question.url }})
  {% endif %}
{% endfor %}


## Data Preparation

{% for question in site.questions %}
  {% if question.step == "data_preparation" %}
- [{{ question.title }}]({{ question.url }})
  {% endif %}
{% endfor %}

## Quality Control

{% for question in site.questions %}
  {% if question.step == "qc" %}
- [{{ question.title }}]({{ question.url }})
  {% endif %}
{% endfor %}

## Analysis

{% for question in site.questions %}
  {% if question.step == "analysis" %}
- [{{ question.title }}]({{ question.url }})
  {% endif %}
{% endfor %}

## Results

{% for question in site.questions %}
  {% if question.step == "results" %}
- [{{ question.title }}]({{ question.url }})
  {% endif %}
{% endfor %}