# Tutorial on genome-scale metabolic networks modelling and Flux Balance Analysis (FBA) using COBRApy and Escher in jupyter ipython notebook

_Author_: Marc Weber  
_Date_: March 2016  
_Affiliation_: Center for Genomic Regulation (CRG), Barcelona, Spain.
_Notes_: This tutorial was created for the course "Whole-cell modeling", taking place at CRG, Barcelona, April 3-8, 2016.

In this tutorial we will learn the basic concepts of flux balance analysis (FBA) and its use in genome-scale metabolic networks of E. coli.

The code will be run in an [jupyter](http://jupyter.org/) ipython notebook taking advantage of the nice interface of jupyter notebooks and the [Escher](https://escher.github.io/) visualization package to draw metabolic maps (see an online example here). We will closely follow some of the exercises from Orth et al. 2010 (supp. tutorial) [1] using the [COBRA package](https://github.com/opencobra/cobrapy) in python. Extensive reference to literature is given in the notebooks along with the code examples.

The tutorial contains two exercises. The first exercise focuses on getting familiar with the COBRA package to compute optimal growth of E. coli under different conditions using FBA and the use of FBA to study single and double gene deletions essentiality. We focus on the central carbon metabolism of the iJO1366 model, which is used as a standard example throughout the tutorial. The second exercise is about metabolic network reconstruction and gap-filling. By comparing model predictions with experimental data on essentiality, failures in the model can be identified in form of gaps and blocked reactions. We lear how to use gap-filling methods to suggest metabolic network completion and add new hypothetical reactions from a universal database.

## Exercise 1: Flux Balance Analysis (FBA)

In this exercise, we will learn to use the COBRA package to compute the optimal growth of E.coli under different conditions using flux balance analysis. We will use the full iJO1366 metabolic model of E.coli (Orth et al. 2011) that takes into accounts 1366 genes, 2251 metabolic reactions and 1136 unique metabolites. We will focus on the glucose central metabolism. The exercises are adapted from the tutorial "What is flux balance analysis?" by Orth, Thiele and Palsson (Orth et al. 2010).

### Outline

- Familiarizing with COBRA and Escher commands.
  - Get and download the iJO1366 from the BiGG database.
  - Loading iJO1366 model.
  - Drawing metabolic map.
  - Altering reaction bounds (adding and/or removing reactions).
  - Change the objective function (typically growth).
  - Solving for fluxes.
  - Draw metabolic map and fluxes using Escher in iPython.
  - Simulating optimal growth.
- Examples:
  - Compute and draw fluxes for aerobic/anaerobic growth on glucose.
  - Growth on alternate substrates
    - compute growth and fluxes on succinate: aerobic / anaerobic (no solution)
    - compute growth and fluxes on puryvate: aerobic / anaerobic (no solution)
  - Simulating different objective function, maximize ATP production.
  - Simulating single gene deletion, gene essentiality
  - Simulating double gene deletions, synthetic lethal

## Exercise 2: Metabolic network reconstruction and gap-filling

### Outline

+ Comparison of model predictions and experimental single gene knockout data
+ False positive predictions
+ False negative predictions and gaps
+ Dead-end metabolites and blocked reactions
+ Gap filling
  - Example 1, E. coli core metabolism and growMatch method
  - Example 2, predict gap-filling reaction for a dead-end metabolite in iJO1366 model
  - Example 3, model-driven discovery of isozymes for iJO1366 false-negative prediction
  - Example 4, reactions from Staphylococcus aureus as universal database for iJO1366 false-negative correction

## Requirements

The notebooks have been tested with:

+ python 3.5

Python packages:

+ jupyter
+ python-libsbml
+ cobra
+ escher

## References

[1] Orth, J. D., Thiele, I., & Palsson, B. Ø. (2010). What is flux balance analysis? Nature Biotechnology, 28(3), 245–248. http://doi.org/10.1038/nbt.1614
