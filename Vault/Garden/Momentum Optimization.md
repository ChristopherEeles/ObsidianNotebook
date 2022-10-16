2022-10-16@13:21

Status: #idea

Tags: [[Machine Learning]] [[Deep Learning]] [[Artifical Intelligence]] [[Stochastic Gradient Descent]] [[Nesterov Accelerated Gradient]]

# Momentum Optimization

## Exponentially Weighted Averages
$$\large
\mathbf{V_t}=\beta\cdot \mathbf{V_{t-1}} + (1 - \beta)\cdot\theta_t
$$

* Where
	* $\mathbf{V_t}$ is the exponentially weighted average at timestep $t$
	* $\beta$ is a smoothing parameter, where steps smoothed over $n \approx \frac{1}{1-\beta}$
	* $\theta_t$ is thw raw output value at timestep $t$
* Effectively smooths noisy data, such as that generated over repeated random samples

## Momentum Optimization
* Used to reduce the volatily of weigth updates in gradient descent
* Also helps efficiently navigate ravines (pathological curvature) in the loss space
	* Accelerates convergence to local minima relative to standard gradient descent (SGD)
* Increases for dimensions whose gradient points int he same direction, reduces update for gradients which change directions

### Algorithm
1. Update the momentum vector ($\large \mathbf{m}$):
	-  $\large \mathbf{m_t} = \beta \cdot \mathbf{m_{t-1}} \cdot \triangledown_{\theta}J(\theta_t)$
2. Update the weights ($\large \mathbf{\theta})$
	* $\large \theta_t = \theta_{t-1} - \eta \cdot \mathbf{m_t}$

### Pseudocode

```python
beta = 0.9
learning_rate = 0.01
momentum = 0
for _ in n_epochs:
	dw = compute_gradient(x, y)  # vector of output wise (neuron wise) gradients
	momentum = beta * momentum + (1 - beta) * dw
	w = w - learning_rate * momentum
```

## Nesterov Accelerated Gradient
* Evaluate the cost function slightly ahead of current position
	*  Measure gradient at $\theta + \beta \mathbf{m}$ instead of $\theta$
* Can be significantly faster than regular momentum optimizations
	* Works due to momentum vector tending to point towards the optimum

---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11.