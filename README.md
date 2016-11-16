# Tutorial on genome-scale metabolic networks modelling and Flux Balance Analysis (FBA) using COBRApy and Escher in jupyter ipython notebook

Author: Marc Weber  
Date: March 2016  
Affiliation: Center for Genomic Regulation (CRG), Barcelona, Spain.
Notes: This tutorial was created for the course "Whole-cell modeling", taking place at CRG, Barcelona, April 3-8, 2016.

In this tutorial we will learn the basic concepts of flux balance analysis (FBA) and its use in genome-scale metabolic networks of E. coli.

The code will be run in an jupyter ipython notebook taking advantage of the nice interface of jupyter notebooks and the [Escher](https://escher.github.io/) visualization package to draw metabolic maps (see an online example here). We will closely follow some of the exercises from Orth et al. 2010 (supp. tutorial) [1] using the [COBRA package](https://github.com/opencobra/cobrapy) in python.

The tutorial contains two exercises. The first exercise focuses on getting familiar with the COBRA package to compute optimal growth of E. coli under different conditions using FBA and the use of FBA to study single and double gene deletions essentiality. We focus on the central carbon metabolism of the iJO1366 model, which is used as a standard example throughout the tutorial. The second exercise is about metabolic network reconstruction and gap-filling. By comparing model predictions with experimental data on essentiality, failures in the model can be identified in form of gaps and blocked reactions. We lear how to use gap-filling methods to suggest metabolic network completion and add new hypothetical reactions from a universal database.

## Requirements

The notebooks have been tested with:

+ python 3.5

Python packages:

+ jupyter
+ python-libsbml
+ cobra
+ escher

## License



## References

[1] Orth, J. D., Thiele, I., & Palsson, B. Ø. (2010). What is flux balance analysis? Nature Biotechnology, 28(3), 245–248. http://doi.org/10.1038/nbt.1614
