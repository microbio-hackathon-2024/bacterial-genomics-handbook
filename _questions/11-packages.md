---
layout: page
title:  "Should I use a package manager like Conda vs Dockerizing or using a VM? What are things to watch out for?"
categories: question
step: analysis
---

- Package managers are great for controlling environments and not completely wrecking your environment with different package versions. Using a manager like Conda, you’re able to isolate different projects to their own environments so the package versions don’t overlap. 
- Using a VM is an alternative to Conda environments (in case Conda can’t be installed) but satisfies the need to isolate different working environments.
- Things to watch out for
    - Not all packages are available for installation through Conda
    - R package installation can get tricky/Conda isn’t great at managing R packages
- A docker container is more likely to be a component in your workflow than to contain your workflow, but whether or not you (or your workflow system) use containers, you should think about containerization - what are my dependencies? Are they difficult to install? Are they shared by other tools in the pipeline? Do different pipeline stages require different versions of the same dependency? Containers can rescue you from dependency hell but it’s better not to go there in the first place.
