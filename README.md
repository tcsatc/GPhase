GPhase: Greedy Approach for Accurate Haplotype Inferencing
==================

Implementation for GPhase algorithm for haplotype inferencing, reported in the paper: "GPhase: Greedy Approach for Accurate Haplotype Inferencing", Kshitij Tayal, Naveen Sivadasan, Rajgopal Srinivasan.

GPhase is primarily a tool for inferring haplotypes from its corresponding SNP genotypes, given a known collection of haplotypes. It is free for both academic and commercial use.

- <h6>GPhase_Parameter.ipynb</h6>Calculation of Model Parameters used by GPhase, namely mutation rate , quadrature points and quadrature weights.This interactive ipython notebook is just for playing around with the parameters. 

- <h6>GPhase_LOOC.py</h6>  GPhase algorithm implementation for leave-one-out cross-validation (LOOCV) where known set of haplotype collection A<sub>n</sub> is created by including all haplotypes except one pair and we infer the constituent haplotype from the combined genotype of remaining pair. Usage: python GPhase_LOOC.py \<arg1\> \<arg2\> . Collection of haplotypes is specified as Arg1 in a comma separated file where each row contains a haplotype, each consisting of l loci. Arg2 specifies number of threads that GPhase uses. Speed of phasing can be improved my multi-threading as many individuals can be phased simultaneously. 

- <h6>GPhase.py</h6>  GPhase algorithm implementation when we have to phase an individual genotype sample, given a collection of known haplotype in the population.Usage: python GPhase.py \<arg1\> \<arg2\> \<arg3\> \<arg4\> . Collection of known haplotypes is specified as Arg1 in a comma separated file where each row contains a haplotype, each consisting of l loci. Similarly sample of individuals to be phased is specified in Arg2 in a comma separated file where each two row contains a random haplotype pair consistent with the genotype, each consisting of l loci. Arg3 specifies the file, where to write the haplotypes estimated by GPhase. Output file is in comma separated format where each two rows contains a haplotype pair, consistent with the genotype inferred by GPhase. Arg4 specifies number of threads that GPhase uses.

- <h6>Minheap.py</h6>  Min Heap implementation for maintaining top-k largest solutions. This file is used by GPhase.py and GPhase_LOOC.py.


-------------------------

If you experience any problem with GPhase or want to ask a question, please feel free to contact me at kshitij@atc.tcs.com and i will be happy to answer them.

Disclaimer:
THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW, EXCEPT WHEN OTHERWISE STATED IN WRITING. THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES PROVIDE THE PROGRAM “AS IS” WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION.
