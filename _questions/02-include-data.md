---
layout: page
title:  "When might I not want to include data?"
categories: question
step: qc
---

There are several cases where you might not want to include data in your final analysis. See below for possibe scenarios: 

## Low or no reads

If your FASTQ files have extremely low to no reads or if the reads are of bad quality and contain high percentage of Ns, using these reads for your analysis can be detrimental. In some cases, certain tools might not work properly or refuse to run. 

Generally, it is good to determine a threshold for minimum read coverage/depth to decide which FASTQ files to discard and/or if sequencing needs to be performed again. In certain cases, even if the FASTQ read counts are low, you can perform sequencing again and combine the FASTQ files to still include the previous data. However, before attempting to do so, assess the quality of the reads before attempting to use them for your analysis. If the reads are erroneous, this can cause issues downstream.


## Too many contigs

After assembling, if your final assembly contains too many contigs, this is a potential sign that something may be wrong with your reads. To assess what ‘too many’ means, compare the contig counts to that of similar sequences. You can use public databases to find similar sequences or any previously assembled sequences for similar organisms/samples. If your contig counts have a large divergence from other similar sequences, it can be a sign that something may have gone wrong in the assembly process or they may be an issue with the reads. 

However, contig count alone is not a good indicator that your assembly needs to be thrown out. To confirm if your assembly is problematic, compare total genome lengths to similar sequences. Generally, if your genome size is not within 10% of the expected size, it may suggest problems with your assembly. However, 10% is not a set threshold so we recommend trying to find a threshold that works best for your sample/organism/project. If you find that your assembly has high contig counts as well as extremely different genome sizes, go back to your reads and assess their quality. We recommend checking for any potential contamination as well. 

In addition, look into the complexity and/or the repetitiveness of your organisms/sequence of interest. If the sequence is known to be tricky to assemble, you may benefit in performing long-read sequencing and doing a hybrid assembly.

## A lot of Ns

If your reads or assembly sequence have a lot of Ns, this is a sign that your reads are not of quality. In this case, we recommend discarding the data or not including the data in your analysis. Ns can be detrimental to any downstream analysis and can drastically alter final results. In cases like this, we recommend re-sequencing the sample if possible.

## Doesn’t taxonomically match to your expectations

If the reads or assembly sequence don’t taxonomically match to your expectations, this is a sign that your sample may be contaminated. 

For example, imagine, you are working with Francisella tularensis samples. You sequence the samples and classify the resulting reads with a taxonomic database. The taxonomic results show that the good percentage of the reads classify as Escherichia coli, this is an indicator that your sample is contaminated. 

One way to confirm contamination is to map the reads to the reference genome of the contaminant. If the reads fully cover the reference genome, then this would indicate that the sample is contaminated. Once you’ve established the sample is contaminated, we recommend not moving forward with the reads as this will drastically alter the final results. It is also good practice to go back and determine the source of contamination. 

For example, here are a couple of questions you can consider: 
- Was it a sample mixup?
- Was the contaminant also sequenced on the same sequencing instrument at the same time?
- Was this contaminant being worked on at the same time in the lab?
- Is the contaminant organism commonly found together with the expected organism?

## Too similar to another genome (overrepresentation of a clone in a dataset)

In very specific cases, for example in GWAS or pangenome studies, you may not want to include all of your datasets. It may not be that the data is bad, but there may be too many datasets that will cause noise. In this case, we recommend down-sampling/de-duplicating your data and removing any datasets that are too similar. 

