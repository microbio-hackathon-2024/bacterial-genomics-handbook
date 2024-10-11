---
layout: page
title:  "When should I invest in long-read sequencing?"
categories: question
step: data_preparation
---

- Generally, short-read or PacBio long reads are sufficient for sequencing an organism as long as the extraction/libraries are adequate
- Long-read is great for trickier genomes, for example, organisms with a high GC content
- The majority of {% glossary phylogenetics %}/population-structure workflows are based on inferring relationships via single-base changes; relatively few are based on large-scale genomic structural change. Therefore most of these pipelines will want you to have accurate short reads and won’t benefit from the structural information in long reads.

