2022-10-16@13:39

Status: #idea

Tags: [[Machine Learning]] [[Artifical Intelligence]] [[Neural Networks]] [[Deep Learning]] [[Optimizer]]
 
# AdaGrad
* Solves problem of widely varying gradient magnitudes
	* Difficult to find a single global learning rate appropriate for the algorithm
	* Sometimes called the elongated bowl problem
		* Gradient Descent goes down steep slope quickly but slows down near the bottom of the valley
* AdaGrad algorithm attemps to solve this by scaling down the gradient vector along the steepest dimensions and scaling up along the flattest dimensions
* Adaptive learning rate:
	* 
* Similar idea to momentum optimization but not using moving averages

## Algorithm
1. Accumulate squared gradient vector ($\large \mathbf{s}$):
	* $\large \mathbf{s_t} = \mathbf{s_{t-1}} + (\triangledown_{\theta}J(\theta_t))^2$
1. Update weights ($\large \theta$):
	* $\large \theta_t = \theta_{t-1} - \eta \cdot \triangledown_{\theta} \otimes \sqrt{\mathbf{s_t} + \epsilon}$
	* $\large \epsilon \approx 10^{-8}$ to prevent dividing by zero





---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11