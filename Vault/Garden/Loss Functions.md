2022-10-02@18:08

Status: #idea

Tags: [[Machine Learning]] [[Artificial Intelligence]] [[Deep Learning]]

# Loss Functions

## Cross-entropy Loss
* Used for binary or multi-class classification
* Average of the true label times the predicted probabilty of the true label for each class
$$\LARGE
\mathcal{L}(\hat Y, Y) = -\frac{1}{M}\sum_{c=1}^M Y \log(\hat Y)
$$
* Where
	* $\hat Y$ is the predicted class probability
	* $Y$ is the $0$ for the wrong class or $1$ for the correct class
	* $M$ is the number of classes




---
# References
1. 