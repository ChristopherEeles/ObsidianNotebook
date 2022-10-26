## Bayesian

* Bayesian techniques allow inclusion of a prior (independent) distribution of information
	* Usually a form of regularization, feature weights
* Typical priors for bayesian neural nets are not very information

## Prior-Data Fitted Network (PFN)

* Similar to transfer learning, but instead of fitting on one dataset and fine tuning we fit a model that is effective at predicting held-out samples from arbitrary subsets of the dataset
* Task for model is to correctly predict a held-out test data-point
	* Not sampling values for our parameters, instead sampling datasets
	* Learn a model $q_{\theta}$ for parameters $\theta$ 
* 