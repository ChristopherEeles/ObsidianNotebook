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
2
3. Adjust bias:
4. Update weights ($\large \theta$):

## Pseudocode


## Use Cases



---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11.