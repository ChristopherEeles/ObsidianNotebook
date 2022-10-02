2022-09-21@22:05

Status: #idea

Tags: [[Machine Learning]] [[Artificial Intelligence]] [[Deep Learning]]

# Activation Functions

## Step Functions
* Applied to a neural network output to determine the state of the artifical neural circuit, common in [[Single Layer Perceptron (SLP)]]s

### Heaviside Function
$$ \large
heaviside(z) = \begin{cases}
	0 \text{ if } z \lt 0 \\
	1 \text{ if } z \ge 0
\end{cases}
$$
### Sign Function
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
* Squahsed output to the range $[-1, 1]$
* Less issue with *vanishing gradient* due to being centered around $0$, but still need techniques to compensate
* Often used in hidden layers
$$\LARGE
\tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}
$$

### ReLU
* Rectified Linear Unit
* Suffers less from *vanishing gradient* less than **sigmoid** or **tanh**
* Instead suffers from *dying ReLU problem* due to $0$ gradient below $0$
* Preferred for hidden layers over **tanh** due to efficient computation
* Also non-differentiable at $x=0$, but rarely an issue due to rarity of the zero case
$$\LARGE
ReLU(x) = \begin{cases}
0 \text{ if } x \lt 0\\
x  \text{  if } x \gt 0\\
\end{cases} = max(0, x)
$$


---
# References
1. [[@geronHandsOnMachineLearning]]: Chapter 10.