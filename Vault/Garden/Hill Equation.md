2022-06-14@17:19

Status: #idea

Tags: [[Dose-Response]] [[Ligand-Binding]] [[Pharmacology]]

# Hill Equation
## Hill-Langmuir Equation[^1]
$$[L_n R]=[R_0]· \frac{[L]^n}{[L]^n + Kd} =[R_0]· \frac{[L]^n}{[L]^n + (K_A)^n} \tag{Hill-1}$$
- Where:
	- $[L_nR]$ is concentration of receptor-ligand complex
	- $[L]$ is total ligand concentration; $[R_0]$ is total receptor concentration (in excess)
	- $k_1$ and $k_2$ are association and dissociation rates;
	- $K_d$ is equillibrium dissociation constant; $K_A$ is $[L]$ for $[L_nR]_{50}$ ($K_A = K_d~iff~n = 1$); 
	- $n$ is the Hill coefficient ($\approx$ binding sites of receptor if positive cooperativity)

- Delineation from __Hill Equation__ which generally refers to the biological response case
	- Dependent variable is \[ligand-receptor\]
- Good approximation of ligand-binding when binding is *specific* and *saturable*
	- Specific: affinity between ligand and receptor is greater for eachother than other materials
	- Saturable: excess of receptor can fully consume ligand such that additional $L$ has little effect on $[L_nR]$
- Assumptions:
	- Binding reaches equillibrium
	- Free ligand concentration $\approx$ total ligand concentration
	- All binding sites of a receptor are simultaneously occupied ($L_nR$ 
- Caveats:
	- If no positive cooperativity, $n$ underestimates binding sites and $K_d$ (or $K_A$) is overestimated
	- If $n << 1$ or $n >> 1$  then $K_d$ (or $K_A$) should be treated with caution 
	- Thus physico-chemical interpretation is only valid if above conditions are met

## Hill Equation

- Delineation from __Hill-Langmuir Equation__ which models ligand-receptor binding
	-  Response is a function of agonist-receptor binding (occupation; _i.e._, the __Hill-Languir Equation__) plus a non-linear signal-transduction factor
	- Derived from __Hill-Langmuir Equation__ by incorporating a signal-transduction function from _occupancy theory_ via _operational model of agonism_[^1]
	* Dependent variable is biological response for this case
* Caveats:
	* The __Hill Equation__ for biological responses is a combination of both mechanistic and empirical parameters and has thus been criticized for excluding a factor for agnoist-receptor activation via conformational change
	* More complex mechanism-based models have been developed 


## Four Parameter Hill Equation[^2]
The most complete form of the Hill equation for stimuli-response curves has four parameters:
$$y = \frac{E_{min} + E_{max}(\frac{x}{m})^\lambda}{1 + (\frac{x}{m})^\lambda} \tag{Hill-3}$$ ^70470f
- Where:
	- $x$ is the dose of the stimuli
	- $E_{min}, E_{max}$ are the minimal and maximal response
	- $m$ is the does required to produce response $\frac{E_{min} + E_{max}}{2}$ (_i.e._, $EC50$) 
	- $\lambda$ is the Hill slope describing the sigmoidicity of the stimuli-response curve. ^2860a8



---

# References

^bb3487

[^1]: [[@gesztelyiHillEquationOrigin2012]]
[^2]: [[@yadavSearchingDrugSynergy2015]]