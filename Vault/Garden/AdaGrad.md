2022-10-16@13:39

Status: #idea

Tags: [[Machine Learning]] [[Artifical Intelligence]] [[Neural Networks]] [[Deep Learning]] [[Optimizer]]
 
# AdaGrad
* Solves problem of widely varying gradient magnitudes
	* Difficult to find a single global learning rate appropriate for the algorithm
	* Sometimes called the elongated bowl problem
		* Gradient Descent goes down steep slope quickly but slows down near the bottom of the valley
* AdaGrad algorithm attemps to solve this by scaling down the gradient vector along the steepest dimensions and scaling up along the flattest dimensions
* **ADA**ptive learning rate:
	* Decays learning rate, but does so faster for steep vs flat dimensions
	* Requires much less tuning of learning rate ($\large \eta$)
* Similar idea to momentum optimization but not using moving averages

## Algorithm
1. Accumulate squared gradient vector ($\large \mathbf{s}$):
	* $\large \mathbf{s_t} = \mathbf{s_{t-1}} + (\triangledown_{\theta}J(\theta_t))^2$
2. Update weights ($\large \theta$):
	* $\large \theta_t = \theta_{t-1} - \eta \cdot \triangledown_{\theta} \oslash \sqrt{\mathbf{s_t} + \epsilon}$
	* $\large \epsilon \approx 10^{-8}$ to prevent dividing by zero

## Pseudocode

```python
grads_squared = 0
learning_rate = 0.01
epsilon= 1e-8
for _ in n_epochs:
	dw = compute_gradient(x, y)
	grads_squared += grads_squared * dw * dw
	w = w - (learning_rate - )
```

## Use Cases
* Works welll for simple quadratic problems, but often stops too early when training neural networks
	* Learning rate scales down before reaching the global optimum


---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11