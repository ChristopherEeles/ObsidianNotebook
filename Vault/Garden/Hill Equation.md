2022-06-14@17:19

Status: #idea

Tags: [[Dose-Response]] [[Ligand-Binding]] [[Pharmacology]] [[Quantitative Pharmacology]]

# Hill Equation
## Hill-Langmuir Equation[^1]
$$\LARGE [L_n R]=[R_0]· \ce{\frac{[L]^n}{[L]^n + Kd} =[R_0]· \frac{[L]^n}{[L]^n + (K_A)^n} \tag{Hill-1}}$$ ^5fd00d
- Dervied from the law of mass action:
$$\LARGE \ce{nL + R <=>[k_1][k_2] L_nR} \tag{Hill-2}$$ ^7edd61
- Where:
	- $\ce{[L_nR]}$ is concentration of receptor-ligand complex
	- $\ce{[L]}$ is total ligand concentration; $\ce{[R_0]}$ is total receptor concentration (significantly exceeded by $\ce{[L]}$)
	- $\ce{k_1}$ and $\ce{k_2}$ are association and dissociation rates;
	- $\ce{K_d}$ is equillibrium dissociation constant ($\ce{K_d \equiv \frac{k_1}{k_2}}$); $\ce{K_A}$ is $\ce{[L]}$ producing $\ce{[L_nR]_{50}}$ ($\ce{K_A = K_d \iff n = 1}$); 
	- $n$ is the Hill coefficient ($\approx$ binding sites of receptor if positive cooperativity and other assumptions met)

- Delineation from __Hill Equation__ which generally refers to the biological response case
	- Dependent variable is \[ligand-receptor\] vs biological response (_i.e.,_ phenotype)
- Good approximation of ligand-binding when binding is *specific* and *saturable*
	- Specific: affinity between ligand and receptor is greater for eachother than other materials
	- Saturable: excess of ligand can fully consume receptors such that additional $\ce{L}$ has little effect on $\ce{[L_nR]}$
- Assumptions:
	- Binding reaches equillibrium
	- Free ligand concentration $\approx$ total ligand concentration
	- All binding sites of a receptor are simultaneously occupied ($\ce{[L_nR] \propto [L]}$; _i.e.,_ no intermediate forms with partial occupancy) 
- Caveats:
	- If no positive cooperativity, $n$ underestimates binding sites and $K_d$ (or $K_A$) is overestimated
	- If $n << 1$ or $n >> 1$  then $K_d$ (or $K_A$) should be treated with caution (_i.e.,_ not interpreted physio-chemically)
	- Thus physico-chemical interpretation is only valid if above conditions are met

## Hill Equation[^1]

- Delineation from __Hill-Langmuir Equation__ which models ligand-receptor binding
	-  Response is a function of agonist-receptor binding (occupation; _i.e._, the __Hill-Languir Equation__) plus a non-linear signal-transduction factor
	- Derived from __Hill-Langmuir Equation__ by incorporating a signal-transduction function from _occupancy theory_ via _operational model of agonism_[^1]
	* Dependent variable is biological response for this case
* Caveats:
	* The __Hill Equation__ for biological responses is a combination of both mechanistic and empirical parameters and has thus been criticized for excluding a factor for agonist-receptor activation via conformational change
	* Due to the non-linear signal transduction factor, the Hill coefficient has a different value and meaning for the biological response case
		* Specifically, $y = f_{tranduction}([L_nR])$ where the transduction function is (1) not readily learnable and (2) almost certainly non-linear (due to the amplifying nature of signalling cascades)
	* More complex mechanism-based models have been developed 


## Four Parameter Hill Equation[^2]
The most complete form of the Hill equation for stimuli-response curves has four parameters:
$$\LARGE \ce{y = \frac{E_{min} + E_{max}(\frac{x}{m})^\lambda}{1 + (\frac{x}{m})^\lambda}} \tag{Hill-3}$$ ^70470f
- Where:
	- $\ce{x}$ is the dose of the stimuli
	- $\ce{E_{min}, E_{max}}$ are the minimal and maximal response
	- $\ce{m}$ is the does required to produce response $\large \ce{\frac{E_{min} + E_{max}}{2}}$ (_i.e._, $\ce{EC50}$) 
	- $\ce{\lambda}$ is the Hill slope describing the sigmoidicity of the stimuli-response curve ^2860a8



---

# References

^bb3487

[^1]: [[@gesztelyiHillEquationOrigin2012]]
[^2]: [[@yadavSearchingDrugSynergy2015]]
[^3]: [[@weissHillEquationRevisited1997]]