# Single-cell genomic variation induced by mutational processes in cancer

[https://www.nature.com/articles/s41586-022-05249-0](https://www.nature.com/articles/s41586-022-05249-0)

## Abstract

### **Biological setup:** 

CRISPR-CAS-engineered cell lines 184-hTERT

* wild-type  
* TP53-deficient
* TP53-deficient;BRCA1-deficient 
* TP53-deficient;BRCA2-deficient mammary epithelial cells (13,818 genomes),

 Also:
 * primary triple-negative breast cancer (TNBC) 
 * high-grade serous ovarian cancer (HGSC) cells (22,057 genomes)

 **scDNA-sequencing**




### **Computational setup:** 



### **Results:** 

Three key patterns of cell-to-cell structural variation, referred to as 'foreground' mutational patterns:

1. **Cell- and Clone-Specific High-Level Amplifications**: These are significant increases in the copy number of DNA segments that were found to be prevalent in tumors with fold-back inversions. These amplifications, especially in known oncogenes, contribute to a high degree of clone-to-clone phenotypic variation within tumors.

2. **Parallel Haplotype-Specific Copy Number Alterations**: These alterations affect one of the two sets of chromosomes and lead to evolutionary diversity within the cancer cell population. They also result in clone-specific mono-allelic expression, where only one allele of a gene is expressed while the other is silenced.

3. **Serrate Structural Variations**: Characterized by variations in the length of copy number segments, these variations were more common in tumors with fold-back inversions and correlated with increased genomic diversity among cell populations.

### **Most relevant parts for me**

1. polyploidization quantification?
2. LOH quantification
3. Allele-specific CNV characterization
4. **HSCN** (haplotype-specific copy number)
5. the construction of phylogenetic trees (Fig. 5a)

### **Figure comments**

&rarr; **Figure 1: characterizing the cell lines**

    a) how was the lineage constructed?
    b-c) WT and TP<sup>-/-</sup> CN are stable, while BRCA1<sup>-/-</sup> high levels of CN variations. 

    haplotype-specific states - how is this done?

    f-k) numeric characterization of CNV states of the cells

&rarr; **Figure 2: case-examples of SV's and CNV alterations**
  
    Some examples of oncogenic alterations due to CN changes; demonstration of breakpoints, etc

They've also looked at **HLAMPs** - high level amplificaions - events when certain regions of DNA are highly amplified, particularly relevant for oncogenes

What is **cnLOH**? (copy neutral heterozygosity?)

**FBI** - fold-back inversion, also called inverted duplication

check HMMCopy (for copy number states) and SIGNALS (for haplotype-specific states)


&rarr; **Figure 3: Tumor samples with similar alterations**

Defining signatures of SV's and CNV's as such -  **HRD-Dup** (enriched in small tandem duplications and BRCA1 mutations), **HRD-Del** (enriched in deletions, BRCA2 mutations), **FBI** (enriched in FBIs and CCNE1 amplification) and **TD** (enriched in large tandem duplications, CDK12 mutations) 
    
    c-e) linking the signature prevalence with "phenotype". By phenotype they mean polyploidy or missegregation or ratios of chromosomal gains vs losses

&rarr; **Figure 4: Linking the aberrations to oncogenic mutations and expression**

    a-c) The phylogenetic trees of the clones

    