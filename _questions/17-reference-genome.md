---
layout: page
title:  "How do I choose a reference?"
categories: question
step: data_preparation
---

To be able to compare samples, it is mandatory to pick a {% glossary reference %} to be able to use reference-based methods. The choice of a 
reference must be done according to several criteria.

## Completeness

Prioritize a genome with minimal gaps or Ns to avoid mapping issues and ensure accurate variant calling.

## Relevance

Choose a reference genome that is relevant to your organism or strain to prevent alignment errors. Analyses that involve multiple alignment to a reference become less sensitive and less accurate if the reference is not sufficiently similar to the rest of your samples.

## Quality

Select a reference with high-quality annotations, well-documented features, and minimal assembly errors for reliable results.

## Ns

Avoid references with excessive Ns to prevent poor mapping and skipped regions, potentially compromising analysis accuracy. Consider using a more complete reference or filling gaps with additional sequencing.

## Metadata

Use a reference with sufficient metadata (strain information, annotations, gene locations) to facilitate result interpretation.

## Version

Use the latest version of the reference genome to benefit from improved assembly, closed gaps, and additional metadata.

## Warnings

Take note of any warning listed for the reference, databases like NCBI will list warnings for a reference if it doesn’t meet certain criteria.