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
* $\phi$ is the activation function
![[Pasted image 20220921221935.png]]


---
# References
1. [[@geronHandsOnMachineLearning]]: Chapter 10.