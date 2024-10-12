---
layout: page
title:  "How computationally intensive do I expect my analysis to be?"
categories: question
step: before_starting
---

![]({{site.baseurl}}/assets/images/06-computational-requirements.svg)

Computational requirements are always varying based on a number of 
parameters, such as the number of samples pr the choice of methods. 
This problem can be approached from both ends: you may want to determine 
the computational requirements for an existing analysis you want to run, 
or you may be trying to design an analysis that can support certain
constraints, like being able to run on a laptop.

## Problem Size

From tge above you get a sense that your computational resources will depend on the amount of data you have, and the complexity of your analysis. 
In most instances, a small dataset of a handful of bacterial genomes can be run on a standard laptop, but hundreds or thousands may require the use of a cloud platform, a cluster, or a bigger server. 

### Number of samples

How many samples are you working with? Most steps of your analysis will have 
to be repeated for each sample, and therefore more samples will require 
longer computation time, and more power. Samples can however quite often be 
processed in parallel, provided several CPU cores are available on the 
machine processing the data.

### Reference-based methods

Reference-based methods often require the use of a {% glossary database %}. 
These databases can sometimes reach very large sizes, which will require a 
substantial amount of storage to be able to run properly. 

### Computational-intensive methods

Some analyses have high computational requirements because they need to process larger amount of data, or tackled computational problems that are harder. For instance, {% glossary phylogenetics %} analyses will require 
substantially more computer resources.

## Benchmarking

To get an estimate of time and resources, create a representative subsample of the unit of your data (e.g. number of assemblies, number of reads, number of contigs) and then run your analysis on a subset in a local environment, or a computing environment you expect to use.  

Measure the total clock time, CPUs used, and memory used and divide it by the number of samples you tested. Sometimes a tool will allow you to adjust your analysis using flags to increase the default number of CPUs or run different components in parallel.

Keep in mind that not all tools and methods will scale the same: most reference
based methods scale linearly in time (it takes twice as long with twice many
sequences), but for instance clustering methods usually scale quadratically 
when an all-versus-all similarity metric is required.