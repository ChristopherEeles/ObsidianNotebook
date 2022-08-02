# BioC2022

## Tuesday, July 27th

### Opening Remarks
* G-DAS: Genomics Data Analytics and Storage
	* Open Storage Network (ONS) based 
* Looking for volunteers to help build dashboards

### KeyNote: Single Cell Transcriptomics
* Sandrine DuDoit, UC Berkley
	* Brian Initiative Census: first catalogue of mammalian human brain cell transcriptomes

#### Olfactory Stem Cells and Neural Regeneration
* Understand stem cell differentiation and regeneration in the olfactory bulb
* Applications in neural tissue damage and degeneration
* p63 as molecular switch of 
* Looking at genetic perturbation from gene knockout (p63) or drug treatment (?)
* Questions: what cell types, differential expression of cells between cell types, what are genes involved in differentiation

#### scRNASeq Workflow
* Exploratory data analysis: EDASeq
* Normalization: RUVSeq, scone
* Dimensionality reduction + regularization: Spare Constrastive Principal Component Analysis (scPCA)
* Expression quantitation: Zero-inflated negative binomial-based wanted variation extration (zinbwave)
	* Use as weights for differential expression analysis
* Resampling-based sequential ensemble clustering (RSEC): clusterexperiment
* Inference of cell lineages and pseudotimes: slingshot
* Trajectory-based differential expression: tradeSeq
* Trajectory inference across multiple conditions: condiments
* Inference of transcription factor activity: transfactor

#### Sample-Level QC
* Read-counts are association with QC metrics (negative correlation)

#### Gene-Level Counts
* See large level of variation in RLE (log-ratio of read count to median overall expression)
* Also correlated with QC metrics

#### Normalization
* Adjust read counts for gene-level (e.g., length, GC-content) and sample-level (e.g., sequencing depth, batch, QC) unwanted technical effects
* The choice of normalization method can have a greater impact on the results (Bullard et tal. 2010)
	* Correct method selection is dataset specific an non-trivial
* `scone` useful package implementing a range of state of the art normalization methods (for read counts?)
* Benchmarked 172 normalization procedures via `scone`: best methods were full quantile normalization and regression on principal components of QC measures
  * Is this benchmark published? Can I find it?
	  * Normalization effectively controls the association of QC metric PC1 vs read-count PC1

#### Cluster Analysis
* Provide a general flexible framework that enables researchers to easily apply and compare a variety of different clustering algorithms and generate a stable consensus clustering
	* RSEC: Resampling-based sequential ensemble clustering; general approach for improving stability; supervised equivalent of bagging/boosting
	* Use cluster-wise differential expression metrics to merge clusterings which are close together; trade of resolution for reproducibility

#### Inference of Cell Lineages and Pseudotimes: Slingshot
* Goal is to identify differential lineages and branches (learn a dendrogram) based on transcriptional clustering
* Sustentacular cells: suporting neuronal cells (glial cells?)

#### Trajectory-Based Differential Expression: tradeSeq
* Infer lineages and pseudotime (temporal ording of cellular states)

#### Inference of Transcription Factor Activity: transfactor
* Define transcription factor activity based on number of mRNA molecular produced across all genes the TF is regulating
* Use tradeSeq to do differential TF activity analysis and identify TF regulating neuronal development

#### 
