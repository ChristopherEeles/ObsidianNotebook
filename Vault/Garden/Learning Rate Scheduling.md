2022-10-16@17:19

Status: #idea

Tags: [[Learning Rate]] [[Optimizer]] [[Deep Learning]] [[Artifical Intelligence]] [[Machine Learning]]

# Learning Rate Scheduling
* Set the learning rate to be some function of the epoch
* Start with high learning rate then reduce once it stops making progress

## Expontential
$$\LARGE
\eta_t = \eta_0 \cdot 0.1^{\frac{t}{s}}
$$
Where:
* $t$ is the epoch and $s$ is decay rate 

## Power

## Piecewise Constant

## 1cycle



---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11.