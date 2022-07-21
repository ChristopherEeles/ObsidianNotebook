vsc2022-07-15@18:21

Status: #idea

Tags: [[Pharmacology]] [[Quantitative Pharmacology]]

# Operational Model of Agonism

### Operational Model of Agonism[^1]

- Developed by Black and Leff to help understand the action of agonists and partial agonists
	- To develop systematic way to measure relative agonist efficacy based on examination of dose-response curves

- Assumes:
	- Agonists bind receptors acording to the law of mass action
	- System is at equillibrium
	- $\ce{[A] >> [R_T]}$; the agonist is in excess of the receptor
$$\large \ce{[AR] = \frac{[R_T][A]}{[A] + K_A}} \tag{OMA-1}$$
- Where:
	- $\ce{[R_T]}$ is total receptor concentration
	- $\ce{K_A}$ is the agonist-receptor equillibrium dissociation constant

- What is the relationship between $\ce{[AR]}$ and response?
	- Don't always know the biochemical details (_.e.g,_ mechanism unknown)

### Black Box Problem[^2]
- Relationship between concentration of activated receptor and biological effect is unknown (a black box)
$$\large \ce{E =} z\ce{([AR]) = }z\ce{\left(\frac{[R_T][A]}{K_A + [A]}\right)} \tag{OMA-2}$$
- Where $\large z$ is some monotonic function relating receptor concentration to observed biological effect (_i.e.,_ phenotype)

### Non-Hyperbolic $\ce{\frac{E}{[A]}}$ Curves[^2]
$$\large \ce{E} = \frac{\ce{E_m[AR]}^n}{\ce{K}^n_E + \ce{[AR]}^n} = \frac{\ce{E_m[R_T]}^n\ce{[A]}^n}{\ce{K}^n_E(\ce{K_A} + \ce{[A]})^n + \ce{[R_T]}^n\ce{[A]}^n} \tag{OMA-3}$$
- Where:
	- $\ce{E_m}$ is the maximal effect possible for a given agonist in the specific tissue

---
# References
[^1]: [[@motulskyFittingModelsBiological2004]]
[^2]: [[@blackOperationalModelsPharmacological1983]]