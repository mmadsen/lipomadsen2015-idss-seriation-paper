# LipoMadsenDunnell 2015 IDSS Seriation Paper #

This repository contains the "source" for the paper "A Theoretically-sufficient and Computationally-Practical Technique for Deterministic Frequency Seriation," by Carl P. Lipo, Mark E. Madsen, and Robert C. Dunnell.  

The paper describes the Iterative Deterministic Seriation Solution (IDSS) algorithm, which has the following features:

1.  It performs frequency seriations with the original artifact type count data, instead of similarity indices between assemblages.
1.  IDSS finds ALL of the possible orderings of assemblages, including valid orders which only use a subset of assemblages.
1.  IDSS can show all of the possible orderings, and employ various graph addition algorithms to superimpose the solutions into a "composite" ordering, which may have many branches (which can occur when an assemblage participates in different seriation solutions).  
1.  The algorithm incorporates a bootstrapped confidence interval calculation for determining pairwise significance of assemblage orders given the sample sizes of each assemblage.  This CI is used when constructing orderings to determine whether assemblage position indicates a different solution, or whether two assemblages are merely interchangeable given sampling error.  

IDSS has many other features either implemented or in development, but the one listed above are specifically described in this paper.  



## IDSS Software ##

The IDSS software itself will continue to evolve, and thus is NOT included in this analysis/paper repository.  

The IDSS software implementation is available at Github in [IDSS](https://github.com/clipo/idss-seriation).  That repository needs to be installed and available on the execution path, along with a Python 2.7 installation (we strongly recommend the [Anaconda Scientific Python](http://continuum.io) distribution, which will make your life a LOT easier).  

The specific release used to perform this analysis (and thus, for readers to replicate it) is [Release V2.0](https://github.com/clipo/idss-seriation/releases/tag/v2.0), available as ZIP or TAR files.  The README inside the archive contains installation information and dependencies.



## Directories ##

The directory **ca-analysis** contains the R code for replicating the correspondence analysis which makes up Figures 2 and 3 in the paper.  The Makefile in this directory simply runs R on the command line, giving it the `CAseriation.r` script, which reads the Phillips, Ford and Griffin assemblage data (as cleaned and verified by Carl Lipo).  The output files are written in the same directory.

The directory **seriation-analysis** contains the same PFG data, and a Makefile which runs the IDSS seriation code to generate Figures 9 through 13 in the paper.  This also serves as a good illustration of how to run the IDSS software on a typical input file.  

The **paper** directory contains the LaTeX source code for the paper itself, as submitted to PLoS One.  

