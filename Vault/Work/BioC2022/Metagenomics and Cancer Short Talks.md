## BioC2022

### A Resource of Micobiome Benchmark Datasets with Biological Ground Truth
* Samuel Gamboa (Waldron Lab at CUNY)

* Identifying microbes associated with a given condition or body ste (biomarkers/signatures)
* Collection of datasets for benchmarking microbiome analysis methods

### BugSigDB: 
* Ludwig Geistlinger Harvard Centre for Computational Biomedicine

* Microbial signature for microbiome in different biological states
	* Microbe set enrichment analysis (data looks similar to gene expression; 16S RNAseq and other methods to identify microbes)
	* Databse will be equivalent of MSigDB for microbiome signatures

* Literature review of >500 papers yields >2000 microbial signatures across different biological conditions and geographical regions
	* Case control design for differential microbiome analysis

* bugsigdbr for R interface via data.frame in R; BugSigDBStats (GitHub) for analyzing this data

* Use cases:
	* Perform enrichment analysis on pooled datasets; more power but potential batch effects?
	* Aggregate gene set rankings from individual datasets

* Ground truths:
	* "Spike-in" studies with positive control
	* Benchmarks via Geistlinger et al. (2021): Towards a gold standard for benchmarking gene set enrichment anlysis

### Similarity metric learning on the L1000 Connectivity Map
* Ian Smith at BHKLab

* Characterize new compounds by similarity to existing perturbation signatues
* Similarity function of two vectors in [-1, 1] where f(A, A) = 1
	* What makes a good similarty metric?
		* There are lots of options
* Uses self-supervised learning to minimize distance between replicate pairs
	* Can interpret as a learned similarity function
	* Or as a transform into a more appropriate similarity space for subsequent clustering analysis

### Diffsig: Assocationg Risk Factors with Mutational Signatures
* Ji-Eun Park at UNC Biostatistics and Genomics Group

* Mutational signature: unique patterns of mutations in DNA
	* Counts of mutation signature in patient populations can be used to learn associations with biological states of interest
* Uses COSMIC and NMF to estimate weights of a signature
	* Many COSMIC signature already have know etiology:
		* Sponteneous deaminiaton of 5-methylcytosie (aging)
		* Activity of the APOBEC family of cytidine ...
* Existing methods:
	* Simple two-group comparisons on existing de novo methods; use Wilcoxon rank sum test, but does not consider inherent uncertainty of estimates
	* HiLDA: Heirarchical Bayesian Diri