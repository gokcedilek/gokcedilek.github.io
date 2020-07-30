---
layout: post
title: Co-op at Bioinformatics Technology Lab
# subtitle: Each post also has a subtitle
# gh-repo: daattali/beautiful-jekyll
# gh-badge: [star, fork, follow]
tags: [bioinformatics][linux][scripting][python][c++][bash]
comments: true
---

Timeline: Jan - Apr 2019

I had a wonderful first co-op experience working 4 months at the [Bioinformatics Technology Lab](http://www.birollab.ca/). The prominent tools and skills I used during my co-op are the Linux (CentOS) operating system and the command-line, scripting, data pipelining, benchmarking, data visualization, multithreading, and the programming languages C++, Python, R, and Bash - along with learning (and sometimes remembering from high school:) some very interesting biology!

I worked on two different projects during my co-op, both of which are described below.

**Project #1:** _Sequence Homology - Antimicrobial Peptide Discovery_

In this project, I followed a procedure/data pipeline for antimicrobial peptide (AMP) discovery using sequence homology tools. AMPs are natural antibiotics; protein sequences that contribute to the innate immune systems of many organisms - [including humans](https://pubmed.ncbi.nlm.nih.gov/24828484/#:~:text=As%20the%20key%20components%20of,warding%20off%20invading%20microbial%20pathogens.&text=These%20peptides%20vary%20from%2010,a%20hydrophobic%20content%20below%2060%25.). The idea behind this project was to investigate "subject" sequences that are similar to given "query" sequences. In this case, this meant investigating protein sequences (subjects) that are similar to known AMP sequences (queries), with the aim of discovering novel AMP sequences from the subject proteins (I worked with the [apis mellifera](https://en.wikipedia.org/wiki/Western_honey_bee) proteins). I wrote Bash and Python scripts to use some widely-used bioinformatics tools such as [BLAST](<https://en.wikipedia.org/wiki/BLAST_(biotechnology)>) and [Jackhmmer](https://en.wikipedia.org/wiki/HMMER), as well as to investigate the results we got from running the tools. After following the data pipeline, the candidate novel AMP sequences I identified in the apis mellifera proteins were either known AMPs, or were declared to be "predicted" AMPs, found on [NCBI](https://www.ncbi.nlm.nih.gov/) - which showed that this introductory workflow I went through worked correctly.

**Project #2:** _Performance Improvement of a Bioinformatics Software Tool_

In this project, I worked on improving the runtime and memory usage of a bioinformatics software program developed at the lab I worked at. As part of this task, I re-implemented the Python code in C++, modularized the code, made some logic changes in the code without changing the functionality of the program, benchmarked the code using various data structure implementations, performed [code profiling](https://github.com/gperftools/gperftools), and wrote a multi-threaded version of the program. For the human chromosomes, which is the largest dataset the program runs on, the runtime improvement was 4.5x, and the memory usage improvement was 1.4x.

You can take a look at the repository which includes some of the highlight pieces of my work at BTL [here](https://github.com/gokcedilek/BCGSC---BTL).
