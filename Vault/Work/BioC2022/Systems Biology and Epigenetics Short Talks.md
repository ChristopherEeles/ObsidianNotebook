# BioC2022

## netZooR: gene regulatory networks
* Quackenbush lab via Harvard T.H. Chan School of Public Health
* https://bioconductor.org/packages/release/bioc/html/netZooR.html
* Inference and analysis of gene regulatory networks
* Transcription factors: proteins that bind to DNA gene and modulate expression
* Not always possible to measure context-specific gene regulatory networks
	* Use contrasts between states to isolate context specific network communities

#### The Network Zoo
* Network reconstruction: PANDA, PUMA, LIONESS, OTTER, SPIDER, EGRET, DRAGON
* Community detection: CONDOR, ALPACA
* Differential analysis: MONSTER, CRANE
* Mutational status predictor: SAMBAR
* netZooR: Harmonizes implementations of all these methods; inteface between methods

#### Network reconstrution methods
* Use multiple layers of omics information and graph comparison methods to infer regulatory network graphs

#### Pipeline:
* Network inference across CCLE cell-lines via panda
* Single-smple networks for epithelial and 
* GRAND database for gene-regulatory networks reconstructed using netZooR
* Netbooks: tutorial notebook server using 

## wcGeneSummary
* Dr. Noriaki Sato; textmining and annotating gene clusters
* Use text-mining to generate gene clusters not listed in pathway databases
	* Summarization fo gene set enrichment analysis results
* Implementation:
	* GeneSummary to retrieve ReqSeq gene summary text
	* Prefilter and preprocessing of input (frequency based, over-reprenation based approaches)
		* N-gram, stopwords, etc.
	* Visulatization" word cloud, correlation network, barplot
	* Anlaysis and integration with other packages
		* Annotate the cluster relationships via Vis.js and Cytoscape.js, text-based clustering
* Use overrepresentation analysis
* Question:
	* What is the input for the querying RefSeq for text? A list of genes?

## Chromophobe: Compare and Constract Chromosome States
* Lauren Harmon (Triche Translational Biological Informatics Lab)

#### Background
* 2.4m of DNA needs to be wound around histones as chromatin
* Jenuwein and Allis (2001): histone code of post-transational modifcations conserved across species
*  Use HMM to infer transition probabilities between histone states (e.g., enhancer, promotor, silencer)
* scChromHMM (Avi's recording): predicts the most likely state that a genome is in at any given location
* chromGene: 

#### chromophobe package
* Still under active development on GitHub but could be useful

## Bisplotti: Graphical Representation of DNA Methylation
* Can be bisulphite or enzyme based: methylated C becomes U, unmethylated stay C
	* In sequencing C becomes T
	* Contrast with normal sequencing to identify methylation regions

#### Global Methylaton Plots
* Show relavive abundace of CpG methylation across samples

#### Multiscale Plots
* Knijnenburg et al (2014): average methylation across many bin widths
	* Compare short and long range methylation in a single plot

#### Read/Fragment Level Methylation
* Uses EpiBED format: BED-compliant information on SNPs of methylation vs normal gene sequencing
* Quasi-single cell resolution as each read is likely to come from a single cell (what?!)

