2022-09-21@22:05

Status: #idea

Tags: [[Machine Learning]] [[Artificial Intelligence]] [[Deep Learning]]

# Activation Functions

## Step Functions
* Applied to a neural network output to determine the state of the artifical neural circuit, common in [[Single Layer Perceptron (SLP)]]s

## Heaviside Function
$$ \large
heaviside(z) = \begin{cases}
	0 \text{ if } z \lt 0 \\
	1 \text{ if } z \ge 0
\end{cases}
$$
## Sign Function
$$\large
sign(z) \begin{cases}
-1 \text{ if } z \lt 0\\
0  \text{  if } z = 0\\
1 \text{  if } z \gt 0
\end{cases}
$$
## Non-Linear Activation Functions
### Sigmoid
* Primary output layer for **binary classification**
* Squashes output to the range $[0, 1]$
* Not used in hidden layers due to *vanishing gradient problem*
$$\LARGE
\sigma(x) = \frac{1}{1 + e^{-x}}
$$

### Tanh

$$\LARGE
\tanh(x) = \frac)
$$

### ReLU

---
# References
1. [[@geronHandsOnMachineLearning]]: Chapter 10.