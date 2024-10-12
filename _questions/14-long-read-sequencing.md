---
layout: page
title:  "When should I invest in long-read sequencing?"
categories: question
step: data_preparation
---

A question that comes up often in the generation and analysis of 
{% glossary sequencing %} data is determining whether to use 
short-read or long-read sequence. 

## Short Reads

Generally, short-read or PacBio long reads are sufficient for sequencing an 
organism as long as the extraction/libraries are adequate.

The majority of {% glossary phylogenetics %} or population-structure workflows 
are based on inferring relationships via single-base changes; relatively few 
are based on large-scale genomic structural change. Therefore most of these 
pipelines will want you to have accurate short reads and won’t benefit from 
the structural information in long reads.

## Long reads

{% for question in site.questions %}
{% if question.slug contains "plasmids" %}
{% assign plasmid_question = question %}
{% endif %}
{% endfor %}

Long-read is great for trickier genomes, for example, organisms with a high GC 
content. They can also help in resolving plasmids 
(see [{{ plasmid_question.title }}]({{ site.baseurl}}{{ plasmid_question.url }})).

