---
layout: page
title:  "How do you quality check sequences? (How do I know a sequence is good)"
categories: question
step: qc
---

## Raw Read Quality Assessment
- Basic sanity check - is the file size correct? If the sequencing is paired, are the forward and reverse read files roughly the same size?

## Trimming and Filtering
- It’s important to be aware of whether your sequencer’s post-processing pipeline trims technical sequence (adapters, barcodes) on its own. Trimming already-trimmed sequences is usually harmless, though.

## Check for Contaminants
- What percentage of your sample/sequences is not expected? 

## Alignment Quality
What are the number of gaps in the alignment? Are there any sequences not aligning? How are your sequences clustering?

## Variant Calling and Analysis
Evaluation of number and types of variants/non-synonymous variants

## Check for Sequence Artifacts

## Genome completeness based on the presence or absence of conserved single-copy ortholog (BUSCO)

## Evaluate Final Assembly Quality
