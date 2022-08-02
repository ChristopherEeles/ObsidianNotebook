## BioC2022

### Unsupervised spatial transcriptiomics analysis defnes molecular anatomy of the human dorsolateral prefrontal cortex
* Molecular anatomy of tissue samples
* Use known microanatomy of the DLPFC (6 layers of grey + 1 of white) as ground truth for cell labels
	* Not possible for larger datasets or in cases where we have no prexisting knowledge
* Unsupervised approaches are needed
	* Spatially aware clustering algorithms
		* BayesSpace: spatial coordinates of spots as prior; encourages spots close together to cluster together (cluster across)
		* SpaGCN: uses histology image of tissue to determine "metagenes"
* Identify the differentially expressed genes in each manually annotated tissue section and correlate with the unsupervised clusters
	* Performance was reasonable
	* K-selection?

### nnSVG: scalable identification of spatially variable genes using nearest-neighbor Gaussian processes
* Lukas Weber at Johns Hoptkins School of Public Health
* SVG: spatially variable genes
* Visium platform: more than one cell per spot
* Why spatially variable genes:
	* Dimension reduction for downstream analysis
	* Identify interesting biomarkers for tissue regions
* Methods
	* SpatialDE: not scalable to large datasets
	* Neatest-neighbour Gaussian Process (NNGP): approximate likely hood with small set of nearest neighbours yielding a spare percision matrix
		* Results in linear scaling with number of spots
		* Much more scalable

### Detecting and quantifying antibody reactivity in PhIP-Seq data with BEER
* PhIP-Seq enables high throughout characterization of antibody response to thousands of target antigens
	* Bacteriophage library expressing peptides of interest
	* Mix serum with bacteriophage probes
	* Capture phages and bound antibody using magnetic A/G beads
	* Gene count matrix using alrignment method of choice
* Use peptide free phages and technical control
* BEER: Bayesian Enrichment Estimation in R
	* Identifying and quantifying antibody reactivity in PhIP-Seq data
	* Genererate matrix of read counts per each query peptide
	* PhIPData object (wrapper around SE)
* Applications in immune therapy prediction?

### Novel framework to discover spatially variable genes
* Simone Tiberi at University of Zurich
* Framework to detect SV genes using spatial clusters
* Use spatial clusters as input; edgeR with spatial cluster as covariate
* Perform spatial clustering: BayesSpace or StLearn
* Benchmark with 2 anchor datasets
	* LIBD (Maynard et al 2020)
	* Melanoma (Thrane et al. 2018)**
* Permute real data to simulate different shapes for the tissue regions
	* Benchmark against range of other methods
	* Performance is better in both TPR and FDR
* Unique features
	* Jointly fit multiple samples for group-level signal
	* Test individual clusters; find tissue cluster specific differentially expressed genes
* 