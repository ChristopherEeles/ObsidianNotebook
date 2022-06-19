2022-06-141554

Status: #idea

Tags: [[Pharmacology]] [[Drug Combinations]] 

# Loewe Additivity

## Classic Loewe Additivity [^1]
Null model must satisfy the equality:
$$\frac{x_1}{X_{Loewe}^1} + \frac{x_2}{X_{Loewe}^2} = 1 \tag{Loewe-1}$$
* Where:
	* $x_1,x_2$ are doses of respective stimuli
	* $X_{Loewe}^1, X_{Loewe}^2$ are the respective doses of individual stimuli need to achieve the biological effect $y_{Loewe}$ of the combined stimuli
	* See Eq. (2)[^1]

Analytic form to compute null prediction for $y_{Loewe}$ with a non-linear solver:

$$\frac{x_1}{m_1(\frac{y_{Loewe} - E_{min}^1}{E_{max}^1 - y_{Loewe}})^{\frac{1}{\lambda_1}}} + \frac{x_2}{m_2(\frac{y_{Loewe} - E_{min}^2}{E_{max}^2 - y_{Loewe}})^{\frac{1}{\lambda_2}}} = 1 \tag{Loewe-2}$$
- Where:
	- $y_{Loewe}$ is the predicted biological effect for doses $x_1 + x_2$ of two respective stimuli under the null hypothesis of Loewe additivity
	- $E_{min}^1,E_{min}^2$ , $E_{max}^1,E_{max}^2$, $m_1,m_2$ and $\lambda_1,\lambda_2$ are the minimal and maximial biological responses, the dose to achieve half maximal response (i.e. $EC50$) and the Hill slope for the dose response curves fitted to the respective individual drug doses
	- See Eq. (7)[^1]

- Assumptions:
	- Individual stimuli-response curves are monotonic
* Limitations
	* Cannot directly assess drug interactions in which the combination effect is higher than the achievable effect of the (sum?) of the individuals drugs

### Loewe Combination Index
$$CI = \frac{x_1}{m_1(\frac{y_c - E_{min}^1}{E_{max}^1 - y_c})^{1/\lambda_1}} + \frac{x_2}{m_2(\frac{y_c - E_{min}^2}{E_{max}^2 - y_c})^{1/\lambda_2}} \tag{Loewe-3}$$



## Biochemically Inuitive Generalized Loewe (BIGL)[^2]


---
# References
[^1]: [[@yadavSearchingDrugSynergy2015]]
[^2]: [[@vanderborghtBIGLBiochemicallyIntuitive2017]]