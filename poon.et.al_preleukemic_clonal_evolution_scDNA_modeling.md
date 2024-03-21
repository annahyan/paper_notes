## Preleukemic clonal evolution revealed using single-cell DNA sequencing and computational modeling

[https://doi.org/10.1101/2023.12.15.571872](https://www.biorxiv.org/content/10.1101/2023.12.15.571872v1)

### Abstract

**Biological setup:** Preleukemic HSCs (pHSC) from 16 AML patients. scDNA sequencing

*How were the pHSCs defined?*

**Computational setup:** Patient-wise **phylogenetic trees** from somatic variants. Simulation and machine learning to model somatic evolution.

*What kind of simulations and machine learning exactly?*

**Results:** Quantification of selection. The variation in the trees can be inferred from the model.

### Most relevant parts for me

1. pHSC selection

Here we define pHSCs based
on being phenotypically-normal HSCs in AML samples. These pHSCs should only harbour early driver mutations, a subset
of the leukemic-specific mutations.


2. The scDNA-seq analysis

The scDNA-seq is **amplicon-based** and target 45 commonly mutated genes in AML. The sorted pHSC population was then put through the commercial microfluidic-based encapsulation platform (‘Tapestri’, by
Mission Bio) during which genomic DNA was barcoded and amplified within single-cell droplets. The panel used was the
catalogue myeloid panel which consists of 312 amplicons (65 kb) that target 45 commonly mutated myeloid genes. **Bult sequencing** was performed additionally for higher confidence VAF estimate and to aid VC.

3. Modeling of the AML

**k-hit staircase model**: 
The model assumes that the HSC's undergo stochastic cell division with a rate $\lambda$ (Poisson distribution), driver mutations are acquired at a rate $\mu$. Driver mutations increase the fitness of the cell by rate $s$. 

The simulation starts with $N$ HSCs, each cell divides symmetrically in $1/\lambda$ years. The simulation is stopped when $K$ mutations are acquired.

For each simuation the tree is recorded and subsampled to $n$ cells to model the subsampling in the HSC single-cell selection process. A neural network is then trained from the trees to infer the correct values for $\mu$ and selection ($s$?).


4. How exactly was the Machine learning used

They have modeled and collected a few thousand trees for each pair of $(\mu, s)$. The pair choices are rather arbitrary - : (10−4, 0%), (10−4, 15%), (10−4, 30%), (10−5, 15%), (10−5, 30%) for k = 4 and (10−4, 0%), (10−4, 15%),
(10−4, 30%), (10−5, 0%) ,(10−5, 15%), (10−5, 30%),(10−6, 15%), (10−6, 30%) for k = 3. For these runs, the clone-size patterns and the trees are recorded. 

The ML model is a dense NN with 4 hidden layers. For each $k$ (the number of required driver mutations) the network predicts the $\mathbf{n}$ vector of clone sizes. 


5. What do we read from the phylogenetic trees?

Essentially the trees just show the succession of acquired driver mutations.
