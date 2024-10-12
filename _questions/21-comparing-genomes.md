---
layout: page
title:  "What are different genomic resolutions I could use for comparison?"
categories: question
step: analysis
---


## Average Nucleotide Identity (ANI)

ANI estimates the overall similarity between the nucleotide sequences of genomes,
typically used to compare bacterial genomes. It provides a percentage of
similarity, with values above 95% often indicating the same species. Hash-based
and fast.

## Multilocus Sequence Typing (MLST)

MLST compares the sequences of genes across different isolates of a species.
MLST schemes are based on a hand-picked selection of conserved “housekeeping”
genes; a scheme is invariably specific to a genus, species, or even subspecies.
In core genome MLST (cgMLST), only the genes found in all strains of a species
(core genome) are compared, providing robust strain-level resolution while
focusing on highly conserved genes. Whole genome MLST (wgMLST), on the other
hand, expands the analysis to include both core and accessory genes, allowing
for a more comprehensive comparison across the entire genome, which can offer
finer differentiation between closely related strains.

## Single Nucleotide Polymorphisms (SNPs)

SNPs represent single base-pair variations between genomes. SNP-based comparisons 
allow high-resolution differentiation of closely related organisms by identifying 
specific mutations across their genomes but are time-consuming to compute and suffer 
reduced accuracy in highly diverse sample sets.
