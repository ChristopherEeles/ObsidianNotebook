2022-06-15@12:22

Status: #idea

Tags: [[Pharmacology]] [[Drug Combinations]] [[Quantitative Pharmacology]]

# Zero Interaction Potency
## Zero Interaction Potency from Response[^1]
![[Hill Equation#^70470f]]

Assuming $E_{max}=1$ and $E_{min}=0$ we can predict the effect from a simplified [[Hill equation]] at dose $x$ as:
$$\LARGE y = \frac{(\frac{x}{m_1})^{\lambda_1}}{1 + (\frac{x}{m_1})^{\lambda_1}}  \tag{ZIP-1}$$ 
Since the Zero Interaction Potency (ZIP) combines the dose-response curve from the [[Loewe Additivity]] model with the [[Bliss Independence]] models, we are able to derive the expected response under the ZIP null model by substituting (ZIP-1) into (Bliss-1):

![[Bliss Independence#^e61386]]

Such that:

$$\LARGE y_{ZIP}= \frac{(\frac{x}{m_1})^{\lambda_1}}{1 + (\frac{x}{m_1})^{\lambda_1}} + \frac{(\frac{x}{m_2})^{\lambda_2}}{1 + (\frac{x}{m_2})^{\lambda_2}} - \frac{(\frac{x}{m_1})^{\lambda_1}}{1 + (\frac{x}{m_1})^{\lambda_1}}\frac{(\frac{x}{m_1})^{\lambda_2}}{1 + (\frac{x}{m_2})^{\lambda_2}} \tag{ZIP-2}$$ 

Where $y$ is predicted the biological response; $\lambda_1$ and $m_1$ are the Hill slope and $EC50$ of the dose-response curve, respectively.

- Assumptions:
	- Individual drugs are equally effective to reach the complete inhibition of cell growth ($E_{min}=0$, $E_{max}=1$)
	- Expected effect of combination should not change the potency of the individual drug dose-response curves under the null hypothesis of no interaction

## Zero Interaction Potency from Viability
To adapt ZIP to be computed from viability instead of response, we need to adjust the equations used to derive it.

In viability assays, such as those assessing the degree of cell killing caused by a specific dose of a compound, the direction of $E_{min}, E_{max}$ are reversed such that a low $E_{max}$ respresents a strong response (i.e., lots of cell killing). Therefore analagous to the assumptions of ZIP for response, we assume $E_{max}=0$ and $E_{min}=1$. 

Substituting into (Hill-3) yields:

$$\LARGE y = \frac{1}{1 + (\frac{x}{m})^\lambda} \tag{ZIP-3}$$

The equation for calculating expected viability under the [[Bliss Independence]] null model is:
![[Bliss Independence#^2828c0]]

Therefore, expected viability under the ZIP null model can be dervied by subsituting (ZIP-3) into (Bliss-7):

$$\LARGE v_{ZIP} = \frac{1}{1 + (\frac{x_1}{m_1})^{\lambda_1}}\frac{1}{1 + (\frac{x_2}{m_2})^{\lambda_2}} \tag{ZIP-4} $$

Since it is rare for a compound to eradicate the entire cell population, especially when being tested in plausibly clinical concentration ranges, the assumption that $E_{max} = 0$ is likely untenable. Therefore it may be more appropriate to use the fully parameterized [[Hill equation]] such that:

$$\LARGE v_{ZIP} = \frac{E_{min}^1 + E_{max}^1(\frac{x_1}{m_1})^{\lambda_1}}{1 + (\frac{x_1}{m_1})^{\lambda_1}}\frac{E_{min}^2 + E_{max}^2(\frac{x_2}{m_2})^{\lambda_2}}{1 + (\frac{x_2}{m_2})^{\lambda_2}} \tag{ZIP-5}$$

```ad-question
Is the assumption that $E_{max}^1 = E_{max}^2$ and $E_{min}^1 = E_{min}^2$ required for $\delta_{ZIP}$ to be interpretable as a "potency shift"? 
```

## ZIP Delta Score[^1]
### Response Case

Reasoned from (ZIP-5) that drug interactions can be modeled as the observed potency shift relative to the ZIP null prediction of biological response to quantify the magnitude and direction of the interaction. Therefore, the expected response when drug 2 is added to 1 drug is:
$$\LARGE y_{1\leftarrow2} = \frac{y_2 + (\frac{x_1}{m_1})^{\lambda_1}}{1 + (\frac{x_1}{m_1})^{\lambda_1}} = \frac{\frac{1}{1 + (\frac{m_2}{x_2})^{\lambda_2}} + (\frac{x_1}{m_1})^{\lambda_1}}{1 + (\frac{x_1}{m_1})^{\lambda_1}} \tag{ZIP-6}$$
```ad-note
$\LARGE y_2 = \frac{1}{1 + (\frac{m_2}{x_2})^{\lambda_2}}$ comes from (A1) of [1].
```
For the fully parameterized Hill equation, this becomes:
$$\LARGE y_{1\leftarrow2} = \frac{E_{min}^1 + y_2 + E_{max}^1(\frac{x}{m_1})^{\lambda_1}}{1 + (\frac{x_1}{m_1})^{\lambda_1}} = \frac{\frac{1}{1 + (\frac{m_2}{x_2})^{\lambda_2}} + (\frac{x_1}{m_1})^{\lambda_1}}{1 + (\frac{x_1}{m_1})^{\lambda_1}} \tag{ZIP-6}$$


### Viability Case



---
# References
[^1]: [[@yadavSearchingDrugSynergy2015]]