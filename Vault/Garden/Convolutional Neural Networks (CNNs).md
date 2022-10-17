2022-10-16@20:15

Status: #idea

Tags: [[Deep Learning]] [[Computer Vision]] [[Artifical Intelligence]] [[Machine Learning]] [[Neural Networks]]

# Convolutional Neural Networks (CNNs)
* In a convolutional layer, neurons are not connected to all elements of their input layer (contrast with a dense layer)
	* Instead they have a "receptive field" of adjacent neurons they connect to
* All neurons in a given layer share their set of weights over all receptive fields
	* Weights represent a mask or filter which detects specific patterns within each layer
	* Additional convolutional layers can assemble basic patterns into complex feature representations

## Zero Padding
![[Pasted image 20221016202757.png]]
* Let $\large f_h$ and $\large f_w$ be the width and height of the receptive field
* A neuron in $\large i^{th}$ row and $\large j^{th}$ column of a given later is connected tot he outputs of neurons $\large i$ to $\large i + f_h - 1$ rows and $\large j$ to $\large j + f_w - 1$ columns
* In order for alyaer to have the same width and height as the previous latyer it is common to add zeros around the inputs

## Stride
![[Pasted image 20221016203316.png]]
* It is also possible to connect a large input layer to a much smaller output layer by spacing out the receptive fields; this is called the stride

## Mathematical Representation
* A really complicated way to say the sum of rows x times columns y
$$\large
\left[
\begin{array}{cccc}
	{x_{11}} & {x_{12}} & {\cdots} & {x_{1 n}} \\
	{x_{21}} & {x_{22}} & {\cdots} & {x_{2 n}} \\
	{\vdots} & {\vdots} & {\ddots} & {\vdots} \\
	{x_{m 1}} & {x_{m 2}} & {\cdots} & {x_{m n}}
\end{array}
\right]
*
\left[
\begin{array}{cccc}
	{y_{11}} & {y_{12}} & {\cdots} & {y_{1 n}} \\
	{y_{21}} & {y_{22}} & {\cdots} & {y_{2 n}} \\
	{\vdots} & {\vdots} & {\ddots} & {\vdots} \\
	{y_{m 1}} & {y_{m 2}} & {\cdots} & {y_{m n}}
\end{array}
\right]
=
\sum_{i=0}^{m-1} \sum_{j=0}^{n-1} x_{(m - i)(n-j)} y_{(1 + i)(1 + j)}
$$


---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 14.