2022-06-15@15:31

Status: #idea

Tags: [[Drug Combinations]] [[Pharmacology]] [[Quantitative Pharmacology]]

# Bliss Independence
$$\LARGE y_{bliss} = y_1 + y_2 - y_1y_2 \tag{Bliss-1}$$ ^e61386
* Where:
	- $y_1,y_2$ are the biological response of two respsective stimuli
	- $y_{bliss}$ is the predicted biological response under the null model of independent mechanisms of effect
- Assumptions:
	- 

## Bliss Independence from Viability
Equation (Bliss-1) specifies the formula for Bliss when computed from response, but it is also possible to to compute this score from viability assays.

Let $r_n$ be response for and $v_n$ be viability for dose-response curve $n$ where $r_n  \in [0, 1]$ and $v_n \in [1, 0]$, such that: $$\LARGE r_n=1-v_n \tag{Bliss-2}$$
In this context we can rewrite (1) as:
$$\LARGE r_{bliss} = r_1 + r_2 - r_1r_2 \tag{Bliss-3}$$

From (2), we can reason that: $$\LARGE v_{bliss} = 1 - r_{bliss} = 1 - r_1 - r_2 + r_1r_2 \tag{Bliss-4}$$
Substituting (2) into (4) we see that:
$$\LARGE v_{bliss} = 1 - (1 - v_1) - (1 - v_2) + (1 - v_1)(1 - v_2) \tag{Bliss-5}$$

Which simplifies to:
$$\LARGE v_{bliss} = 1 - 1 + v_2 - 1 + v_2 + 1 - v_2 - v_1 + v_1v_2 = v_1v_2 \tag{Bliss-6}$$

 Therefore we compute the predicted viability under the Bliss Independence (null) model as: 
 
 $$\LARGE v_{bliss} = v_1v_2 \tag{Bliss-7}$$ ^2828c0

Synergy under this model is therefore defined as $\large v_{observed} < v_{bliss}$.

---
# References
1. 
2. [[@huangPharmacometricsScienceQuantitative2007]]