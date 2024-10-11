---
layout: page
title:  "How computationally intensive do I expect my analysis to be?"
categories: question
step: before_starting
---

Computational requirements are always vary based on a number of parameters,
such as the number of samples pr the choice of methods. This problem can
be approached from both ends: you may want to determine the computational
requirements for an existing analysis you want to run, or you may be trying
to design an analysis that can support certain constraints, like being able 
to run on a laptop.

## Number of samples

How many samples are you working with? Most steps of your analysis will have 
to be repeated for each sample, and therefore more samples will require 
longer computation time, and more power. Samples can however quite often be 
processed in parallel, provided several CPU cores are available on the 
machine processing the data.

## Reference-based methods

Reference-based methods often require the use of a database. These databases
can sometimes reach very large sizes, which will require a substantial amount
of storage to be able to run properly. 

## Computational-intensive methods

Some analyses have high computational requirements because they need to process larger amount of data, or tackled computational problems that are harder. For instance, {% term phylogenetics %} analyses will require 
substantially more computer resources.
