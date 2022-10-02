2022-10-02@15:34

Status: #idea

Tags: [[Artificial Intelligence]] [[Deep Learnig]] [[Neural Networks]] [[Threshold Logical Unit]] [[Single Layer Perceptron (SLP)]]

# Multilayer Perceptron

## Multilayer Perceptron (MLP)
* MLPs overcome the XOR classification issue for SLPs!
![[Pasted image 20221002151903.png]]
### MLP XOR
$$
\begin{aligned}
	\mbox{Let } L1.1 := heaviside(x_1 + x_2 - 1.5) = y_1 \\
	\mbox{Let } L1.2 := heaviside(x_1 + x_2 - 0.5) = y_2\\
	\mbox{Let } L2 := heaviside(-y_1 + y_2 - 0.5)= y_3 \\
\end{aligned}
$$
1. XOR case
$$
\begin{aligned}
\mbox{Let } x_1=1,x_2=0 \\
y_1 = heaviside(1 + 0 -1.5) = 0 \\
y_2 = heaviside(1 + 0 - 0.5) = 1 \\
y_2 = heaviside(-0 + 1 - 0.5) = 1
\end{aligned}
$$
2. OR case
$$
\begin{aligned}
\mbox{Let } x_1=1,x_2=1 \\
y_1 = heaviside(1 + 1 -1.5) = 1 \\
y_2 = heaviside(1 + 1 - 0.5) = 1 \\
y_2 = heaviside(-1 + 1 - 0.5) = 0
\end{aligned}
$$






---
# References
1. 