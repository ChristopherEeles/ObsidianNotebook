2022-09-21@22:15

Status: #idea

Tags: [[Artificial Intelligence]] [[Deep Learnig]] [[Neural Networks]] [[Threshold Logical Unit]]

# Perceptron
* Composed of multiple [[Threshold Logical Unit]] with each TLO conected to all the inputs
* Layers with connections to all the layers are called *fully connected* or *dense* layers:
$$\large
h_{\boldsymbol{W},\boldsymbol{b}}(\boldsymbol{X})=\phi(\boldsymbol{X}\boldsymbol{W} + \boldsymbol{b})
$$
Where:
* $\boldsymbol{X}$ is the matrix of input features with one row per instance and one column per feature
* $\boldsymbol{W}$ is the matrix of all connection weights except the bias neuron
* $\boldsymbol{b}$ contains all the connection wieghts between the bias neuron and the articial neuron, with one bias term per neuron
* $\phi$ is the activation function, which converts the continuous output of the neural network into a state for each neuron
![[Pasted image 20220921221935.png]]

### Perceptron Learning
* Applies Hebbian Learning, inspired by the Hebb Rule: "neurons that fire togther, wire togther"
	* Rule by Donald Hebb (1949), quote by Seigird Lowel
$$\LARGE
w_{i,j}^{\mbox{\small (next step)}} = w_{i,j} + η(y_i - \hat y_j)x_i
$$
* Where:
	* $w_{i,j}$ is the connection weight betwen the $i^{th}$ input neuron on the $j^{th}$ output neuron
	* $x_i$ is the $i^{th}$ input value of the current training instance
	* $\hat y_j$ is the output of the $j^{th}$ output neuron for the curren training instance
	* $y_i$ is the target output for the $j^{th}$ output neuron for the curren training instance
	* $η$ is the learning rate
* *Perceptron convergence theorem*: Roenseblatt provided that of the training instances are linearly separable, this algorithm will always converge to a solution.

## Single Layer Perceptron (SLP) Limitations
* Due to a linear activation function, Single Layer Perceptrons are incapable of learning complex (i.e., non-linear) patterns
	* Similar to Logistic Regression but outputting a hard prediction rather than a class probability
		* May be a reason to prefer Logistic Regression of SLP
* 
---
# References
1. [[@geronHandsOnMachineLearning]]: Chapter 10