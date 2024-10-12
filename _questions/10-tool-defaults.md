---
layout: page
title:  "Should I change tool defaults?"
categories: question
step: analysis
---

Some bioinformatics tools have internal default settings for things like 
quality scores, percentage of sequence similarity, or size of different 
components of sequence data. Default settings could be put into place because 
of tool testing or benchmarking analysis, but they do not necessarily apply to 
all datasets. It’s likely that defaults have been set assuming a certain type 
of input data and analytical aim. If your input data or analytical aims diverge 
significantly from the software authors, changing defaults could help to perform 
more appropriate analysis. Before you use a tool, get familiar with its purpose 
and why it has certain settings.

## Testing

There are different ways to test the boundaries of a tool’s default. To get 
started with your own testing:  

1. Read the developers documentation: Documentation formats include wiki pages, 
   Github repositories, other code repositories, published papers, static 
   tutorials, or the `--help` option for tools run on a command line. 
2. Check out what the use case was for the tool and its original purpose. Some 
   tools might have been developed with one organism in mind, but it could be 
   adapted based on  
3. Create a small test set of your own data and see how similar your results are 
   at different cutoffs. For example, if a tool has a setting that will analyze 
   reads only with a Q30, try adjusting to Q40 or Q20. You may also try the tool 
   at the different defaults and then use it in a downstream analysis. How do 
   the downstream results change?

## Heuristics

Tools that are {% glossary heuristic %} usually have different profiles for 
favoring accuracy over speed. For instance, the DIAMOND protein aligner offers
a `--sensitive` flag and a `--fast` flag depending on the desired trade-off.