2022-10-16@14:13

Status: #idea

Tags: [[Machine Learning]] [[Neural Networks]] [[Optimizer]] [[Artifical Intelligence]] [[Deep Learning]]

# Adam
*  ADAptive Moment estimation
	* Keeps track of exponentially decaying averages of past gradients like [[Momentum Optimization]]
	* Keeps track of exponentially decaying averages of past squared gradients like [[RMSProp Optimization]]
* Adaptive learning rate algorithm, therefore requires much less tuning of learning rate ($\large \eta$)

## Algorithm

1. Update momentum ($\large \mathbf{m}$) and squared gradients ($\large \mathbf{s}$) vectors:
	* $\large \mathbf{m_t} = \beta_1 \cdot \mathbf{m_{t-1}} + (1 - \beta_1) \triangledown_{\theta}J(\theta_t)$
	* $\large \mathbf{s_t} = \beta_2 \cdot \mathbf{s_{t-1}} + (1 - \beta_2) (\triangledown_{\theta}J(\theta_t))^2$
2. Adjust bias:
	* $\large \mathbf{m_t} = \frac{\mathbf{m_t}}{1 - \beta_1^t}$
	* $\large \mathbf{s_t} = \frac{\mathbf{s_t}}{1 - \beta_2^t}$
3. Update weights ($\large \theta$):
	* $\large \theta_t = \theta_{t-1} - \eta \cdot \mathbf{m_t} \oslash \sqrt{\mathbf{s_t} + \epsilon}$

## Pseudocode

```python
grads_squared = 0
beta1 = 0.9
beta2 = 0.99
learning_rate = 0.01
epsilon = 1e-8
grads_momentum = 0
grads_squared = 0
for i in range(1, n_epochs + 1):
	# calculate gradients
	dw = compute_gradient(x, y)
	# Calcualte momentum and RMSprop averages
	grads_momentum = beta1 * grads_momentum + (1 - beta1) * dw
	grads_squared = beta2 * grads_square + (1 - beta2) * dw * dw
	# Fix bias
	grads_momentum = grads_momentum / (1 - beta1 ** i)
	grads_squared = grads_squared / (1 - beta2 ** i)
	# Update weights
	w = w - (learning_rate / np.sqrt(grads_squared + epsilon)) * grads_momentum
```

## Use Cases


---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11.