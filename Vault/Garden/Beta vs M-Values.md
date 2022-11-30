2022-11-30@11:22

Status: #idea

Tags: [[Methylation]] [[Epigenetics]] [[Microarray]]

# Beta vs M-Values

## Beta Value

* Beta-value is the ratio of methylated probe intensity to overall intensity
* The beta-value for the $i^{th}$ CpG site is:

$$\large
Beta_i = \frac{max(y_{i,meth}, 0)}{max(y_{i,unmeth,0}) + max(y_{i,meth},0)) + \alpha} 
$$
* Where:
	* $y_{i,meth}$ and $y_{i,unmeth}$ are the intensity of the $i^{th}$ methylated and unmethylated probes, repectively
	* $\alpha$ is a constant added to prevent dividing by zero (or very nearly zero; default is 100)

## M-Values

* M-values are the $log_2$ ratio of the methylated vs unmethylated probes
* The m-value for the $i^{th}$ CpG site is:

$$\large
M_i = log_2\left(\frac{max(y_{i,meth}, 0) + \alpha}{max(y_{i,unmeth,0} + \alpha}\right)
$$
## Converting Between M- and B-Values

$$\large
Beta_i = \frac{2^{M_i}}{2^{M_i} + 1}; M_i = log_2\left(\frac{Beta_i}{1 - Beta_i}\right)
$$

---
# References
1. [[@duComparisonBetavalueMvalue2010]]