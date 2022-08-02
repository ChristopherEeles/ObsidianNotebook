## BioC2022
### Assessing cellular heterogeniety across time and disease
* Jalees Rehman, MD at University of Illinois College of Medicine

* Computation approaches to study tissue injury
* Blood vessels of the lung have the strongest inflammatory/immune response to LPS toxin in mice
	* Also have the highest baseline level of inflammation; helps defend against pathogens but can results in over reaction
* Studying endothelial heterogeniety following inflammatory injury with LPS via scRNA-Seq
* Subpopulation of inflammatory and developmentally primed endothelial cells
	* See third subpopulation associated with proliferation develops days after injurt
		* Likely arise from developmentally primed endothelial cells
	* Interested indetermining what TFs drive the shift in subpopulations
* Bayesian Inference Transcription Factor Activity Model for Analysis of Single Cell Transcriptomes (BITFAM)
	* Input ChIP-Seq data with normalized scRNA-seq
	* Learn gene weights basedon ChIP-Seq based TFs
		* Maybe TF expression is a better marker of cell identity than
	* Caveat: quality of your prior for TF weights is dependent on the quality of ChIP-seq data
* When using the top 100 weighted TF targets for enrichment analysis you get much more biologically information results then the full set of potential targets
* Can infer cell types reliably from TF activities alone
	* Not intended as a clustering benchmark

* Intersect ChIP-seq with ATAC-seq to integrate chromatin accessibility prior knowledge

* TrendCatcher: Analysis Platform for Gene Expression Dynamics
	* Works well for relatively stable cell populations
		* So not for cancer? Due to instability of cellular heterogeniety

* Also want to look for dynamism of ssATAC-seq data
	* Answer the question accessible where using annotations for gene subcompnent and cis-regulatory elements
	* Does genomic distance between accessible regions define cell states?
	* How do you validate TF gene weights?
	* Are the weights time dependent?
		* Integration of dynamic chromatin accessibility
		* Validate with CRISPR-Cas9 TF deletion studies