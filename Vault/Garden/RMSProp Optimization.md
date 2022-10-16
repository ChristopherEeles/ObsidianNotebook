2022-10-16@13:51

Status: #idea

Tags: [[Machine Learning]] [[Neural Networks]] [[Artifical Intelligence]] [[Optimizer]] [[Deep Learning]]

# RMSProp
* Solves early stopping issues with [[AdaGrad Optimization]] by taking an exponentially weighted average of squared gradients
	* Applying momentum optimization via exponentially weighted averages to the AdaGrad algorithm
	* Get adaptive learning rate along with momentum
* RMS = Root mean squared

## Algorithm
1. Update squared gradient vector ($\large \mathbf{s}$):
	* $\large \mathbf{s_t} = \beta \cdot \mathbf{s_{t-1}} + (1 - \beta) \cdot (\triangledown_{\theta}J(\theta_t))^2$
1. Update weights ($\large \theta$):
	* $\large \theta_t = \theta_{t-1} + \eta \cdot \triangledown_{\theta} J(\theta_t) \oslash \sqrt{\mathbf{s_t} + \epsilon}$

## Pseudocode

```python
grads_squared = 0
beta = 0.9
learning_rate = 0.01
epsilon = 1e-8
for _ in n_epochs:
	dw = compute_gradient(x, y)
	grads_squared = beta * grads_squared + (1 - beta) * dw * dw
	w = w - (learning_rate / np.sqrt(grads_squared + epsilon)) * dw
```

## Use Cases
* Works well for regression tasks with deep neural networks
---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11.