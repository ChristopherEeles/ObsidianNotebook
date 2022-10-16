2022-10-16@14:31

Status: #idea

Tags: [[Optimizer]] [[Deep Learning]] [[Artifical Intelligence]] [[Neural Networks]] [[Machine Learning]]

# Adamax
* Same algoirthm as [[Adam Optimization]] except the weight updates are scaled by the $\large \ell_{\inf}$ norm instead of the $\large \ell_2$ norm in the weight update step:
	* Adam:![[Adam Optimization#^0e83bb]]
	* Adamax:
		* $\large \theta_t = \theta_{t-1} - \eta \cdot \mathbf{m_t} \oslash \max(s_t)$






---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11.