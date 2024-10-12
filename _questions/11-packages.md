---
layout: page
title:  "How can I make sure my analysis can be setup on any host machine?"
categories: question
step: analysis
---

While developing an analysis for your data, you will most likely integrate
other tools. You must make sure that you are declaring these dependencies, 
so that other users can install them when needed.

## Language-specific Packages

Package managers are great for controlling environments and not completely 
wrecking your environment with different package versions. Langugage specific
package managers (like `pip` for Python, `gem` for Ruby or CRAN for R) can 
be used if all the dependencies of your code are available in just one language. 

## Language-agnostic Packages

Quite often in bioinformatics, the dependencies are not all in the same 
place, in particular when binary tools are needed. Some tools may be written
in C++ and have to be compiled, some are Perl or Python scripts, and there
is no easy way to get them all together in a language-specific package manager.

In that case, more generic package manager like Conda let you install 
dependencies in binary form into their own environments. Making separate 
environments for separate projects also help managing and isolating package versions. For Conda, the [Bioconda](https://bioconda.github.io/) channel
hosts the most common bioinformatics packages.

If using Conda, make sure to pin your dependencies *all* through Conda, 
as mixing them with other package managers can make a mess of your 
project environment.


## Containers

In the case where your dependencies are even harder to manage, you may wish
to build a {% glossary container %}. Common formats include Docker and Apptainer (formerly Singularity).

Containers allow to package code and all its dependencies into a filesystem
completely isolated for the host. They allow freezing dependencies, at the
cost of a larger storage footprint. 

Note that some HPC may ban the use of containers for safety reasons, so 
it may be best to assess first where you intend your code to run
(see the [Computational requirements]({{ site.baseurl }}/questions/06-computation-requirements.html) section first). Containers can rescue you from dependency hell but it’s better not to go there if there is a more
reasonable option.

## Virtual Machine

Using a virtual machine (VM) is an alternative to Conda environments (in case Conda can’t be installed) but satisfies the need to isolate different working environments. Virtual machines are quite often impossible to share
between platforms, so it's recommended to avoid them to make the analysis 
more reproducible.
