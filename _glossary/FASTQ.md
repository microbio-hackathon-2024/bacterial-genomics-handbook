---
layout: glossary
title:  "FASTQ"
categories: glossary
definition: "A standard file format for storing raw sequencing data and the corresponding quality."
---

Each entry in a FASTQ file consists of four lines: the first line contains a sequence identifier (starting with '@'), the second line contains the nucleotide sequence, the third line is a '+' separator (sometimes repeating the identifier), and the fourth line contains a string of quality scores (in ASCII) that correspond to the reliability of each nucleotide in the sequence. FASTQ files are essential for downstream analysis in genomics, as they provide both the sequence data and an indication of its accuracy.

