2022-10-16@18:55

Status: #idea

Tags: [[Regularization]] [[Deep Learning]] [[Artifical Intelligence]] [[Neural Networks]]

# Dropout
* Regularization technique proposed by Geoff Hinton in 2012

## Algorithm
* At every training step (including input neurons but excluding output neurons) has a probability, $\large p$, of being temporarily "dropped out" (deactivated) until the next training step
* The hyperparameter $\large p$ is called the drop-out rate and is typically set to 50%
	* After training, neurons do not get dropped out anymore!

## Inference
* After training with a 50% drop-out rate, each neuron will be connected to twice as many neurons as it was in training at inference time
* To compensate for this, the weights of each neuron must be scaled down
	* General rule is to multiple each input connections weight by $\large (1 - p)$ after training




---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11.