2022-10-16@17:19

Status: #idea

Tags: [[Learning Rate]] [[Optimizer]] [[Deep Learning]] [[Artifical Intelligence]] [[Machine Learning]]

# Learning Rate Scheduling
* Set the learning rate to be some function of the epoch
* Start with high learning rate then reduce once it stops making progress

## Exponential
$$\LARGE
\eta_t = \eta_0 \cdot 0.1^{\frac{t}{s}}
$$
* Where:
	* $t$ is the epoch and $s$ is decay rate 
* Works well but need to tune both $\large \eta_0$ and $\large s$

## Power
$$\LARGE
\eta_t = \frac{\eta_0}{(1 + \frac{t}{s})^c}
$$
* Where:
	* $\large c$ is a rate contant generally set to 1

## Piecewise Constant
$$\LARGE
\eta_t = \begin{cases}
		\eta_0 &\text{if} \, t \lt n_0 \\
		\eta_1 &\text{if} \, n_0 \ge t \lt n_1 \\
		... \\
		\eta_n &\text{if} \, n_{n-1} \le t
	\end{cases}
$$
* Predefined intervals to change learning rate over
* Can work well but requires lots of manual tuning to figure out when to adjust the rates

## Performance Scheduling
* Measure validation error every $N$ steps and reduce learning rate by a factor $\large \lambda$ when the error stops dropping 

## 1cycle
* Grows the learning rate $\large \eta_0$ linearly up to $\large \eta_1$ half way through training
* Then decrease the learning rate linearly to $\large \eta_0$ during the second half of traing 


---
# References
1. [[@geronHandsOnMachineLearning]]. Chapter 11.