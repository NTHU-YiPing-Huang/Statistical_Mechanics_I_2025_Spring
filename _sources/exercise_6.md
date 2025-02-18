# Exercise 6

```{admonition} Problem 1: Change of basis in second quantization
:name: Prob_6-1
:class: tip

We can represent quantum operators in different basis when we use the first quantized expression. We have formulated second quantization during the lecture. Let's consider the second quantized operator for kinetic energy for free particles in a one dimensional box with length $L$. That is,

$$
	\widehat{H}_{kin}=\sum_{k,k'}a^{\dagger}_{k}\{k|\frac{\widehat{P}^2}{2m}|k'\} a_{k'}=\sum_{k}\frac{(\hbar k)^2}{2m} \widehat{n}_k
$$
Here, we use $|k\}$ to represent the single particle ket for eigen basis of momentum operator. $\widehat{P}|k\}=\hbar k|k\}$ and $\{x|k\}=\frac{1}{\sqrt{L}} e^{ikx}$.
Suppose we need to change the basis into a basis formed by $|\alpha\}$. Here, $\{x|\alpha \}=f_{\alpha}(x)$. $\alpha^{\dagger}_{k}/a_{k}$ are the rising and lowering operator for the single particle mode $k$.

1. How to change the basis to express $|k\}$ using the basis $|\alpha\}$ in first quantization expression? Express your result using $f_{\alpha}(x)$ and required operations. (Hint: we want to express our result where $x$ is considered as a dummy index. We can do that by inserting compete set $\sum_{\alpha}|\alpha\}\{\alpha|$ first. Then, insert complete set $\int_0^L dx |x\}\{x|$ to express $\{\alpha|k\}$.)
2. How to change the basis of a second quantized Hamiltonian? Find $c_{\alpha}(k)$ in $a^{\dagger}_{k}=\sum_{\alpha}c_{\alpha}(k)a^{\dagger}_{\alpha}$. (Hint: We can find it by comparing $\widehat{H}_{kin}=\sum_{\alpha,\alpha'}a^{\dagger}_{\alpha}\{\alpha|\frac{\widehat{P}^2}{2m}|\alpha'\}a_{\alpha'}$ and the change of basis process in the previous question.)
3. Express the second quantized operator $\widehat{H}_{kin}$ in the real space representation.
```

```{admonition} Problem 2: 1D Ising model bit by bit
:name: Prob_6-2
:class: tip

1. Exact calculation of a three-spin Ising model (Open boundary condition):
The Hamiltonian is $H_{3spins}=-J(s_1s_2+s_2s_3)$, $s_i=\pm1$.

	1. Find all the configurations.
	2. Calculate the corresponding energy of each configuration.
	3. Write down the partition function of the three-spin Ising model.
	
2. Now consider an Ising chain with $N$ spins. Let's assume we ignore the boundary effects. $H(\left\{ s_i \right\})=-J\sum_{i}s_is_{i+1}$. Here $\beta J\equiv K$.
	
	```{figure} /images/decimation.pdf	
	---
	width: 600px
	name: fig-1DIsing
	---
	Step by step decimation process for one-dimensional Ising model.
	```
	
	Above calculation sum over all the spin configurations all at once. Now we try to see if we can calculate the partition function in a different way.

	1. Suppose we start from the spin chain as in Fig.\ref{fig:1DIsing} (a). We divide the spins using the three-spin clusters. Now consider the spins between two successive black spins (The grey part of the figure), $s'_{i}$ and $s'_{i+1}$. The factors in the partition function summation related to these spins are
	
	$$
	e^{K s'_{i}s_{b}}e^{K s_{b}s_{r}}e^{K s_{r}s'_{i+1}}
	$$
	
	, where $s_{b}$ and $s_{r}$ represent the blue and red spins between the $s'_{i}$ and $s'_{i+1}$. And we use $K=\beta J$ for our convenience One can express $e^{K s_{b}s_{r}}$ as

	$$
	e^{K s_{b}s_{r}}=\cosh \left( K \right) (1+x s_{b}s_{r})\text{.}\label{Bfactor}
	$$
	
	Find the expression of $x$. Use $K$ (without $s_r$ and $s_b$) to express your answer. (Hint: use the even/oddness of $\sinh x$ and $\cosh x$. )
	
	2. Use the result of the above expression to simplify the expression
	
	$$
	\sum_{s_{b}=\pm1}\sum_{s_{r}=\pm1}e^{K s'_{i}s_{b}}e^{K s_{b}s_{r}}e^{K s_{r}s'_{i+1}}=2^{n}\left( \cosh K \right)^3\left( 1+g(x)s_i's_{i+1}' \right)=e^{K's_{i}'s_{i+1}'}\text{.}\label{3spinZ}
	$$
	
	Find $n$ and $g(x)$. (Hint: expand the expression using (\ref{Bfactor}) and use the fact that terms proportional with odd powers of $s_i$ vanishes.)
	
	3. Comparing Eq. (\ref{3spinZ}) and Eq. (\ref{Bfactor}), the forms are very similar. If we ignore the pre factors, the $\cosh K$ in (\ref{Bfactor}) and $2^{n}(\cosh K)^3$ in (\ref{3spinZ}), we can build the relation between $K$ and $K'$ (or equivalently $x$ and $g(x)$). Find the relation between $K$ and $K'$.
	
	4. When we sum over $s_b$ and $s_r$, the partition function can be considered as a partition function of coupled black spins $\left\{ s'_{i} \right\}$. (Because we have a sum of products of $\left\{ s'_{i} \right\}$ in the partition function with certain coefficients that capture how the black spins are coupled.)
	Formally, we go from the original partition function 

	$$
	Z\Big|_{ \left\{ s_i \right\}} = \sum_{ \left\{ s_i \right\} }e^{-\beta H(\left\{ s_i \right\})}
	$$
	
	where $\Big|_{ \left\{ s_i \right\}}$ means the statistical variables are $\left\{ s_i \right\}$.
Now we keep the black spins intact and sum over the blue and red spins.

	$$
	Z\Big|_{ \left\{ s_i \right\}}= \sum_{ \left\{ s_i \right\} }e^{-\beta H(\left\{ s_i \right\})}=\sum_{ \left\{ s'_{i} \right\}}\left[\sum_{ \left\{ s_{b,i} \right\}}\sum_{ \left\{ s_{r,i} \right\}}e^{-\beta H(\left\{ s_i \right\})}\right]=\sum_{ \left\{ s'_{i} \right\}}e^{-\beta H'\left( \left\{ s'_{i} \right\} \right)}
	=Z\Big|_{ \left\{ s'_i \right\}}
	$$
	
	Here $H'( \left\{ s'_{i} \right\})$ might not have the same expression as $H(\left\{ s_i \right\})$. Use Eq. (\ref{3spinZ}) and derive the expression of $H'(\left\{ s'_{i} \right\})$. (Hint: The nearest neighbor Boltzmann factor is expressed as $e^{K's_i's_{i+1}'}=\cosh K' \left( 1+x s_{i}'s_{i+1}' \right)$. Compare this expression with Eq. (\ref{3spinZ}) to have a hint about the possible expression. $\beta H'(\left\{ s'_{i} \right\})=Ng(K,K')-K'\sum_{i}s'_{i}s'_{i+1}$. Here $N$ is the total number of the original sites. Find the expression of $g(K,K')$.)
	
	5. From the above expression, we know the new Hamiltonian $H'(\left\{ s_{i}' \right\})$ has the same form as the original one. Except for the coupling constant, which is related to the new value $K'$, and the constant term, which is independent of the $\left\{ s_{i} \right\}$, the Hamiltonian is basically equivalent with the original Hamiltonian. The term that is independent of $\{s'_{i}\}$ will not affect the calculation of the expectation value. However, it could influence the calculation of the free energy. We can now try to iterate this process by dividing $\left\{ s'_{i} \right\}$ into three-spin clusters again as in Fig. \ref{fig:1DIsing}(b) and sum over the blue and red spins, $s'_{b,i}$ and $s'_{r,i}$. Then the Hamiltonian will be expressed by the black spins in Fig.\ref{fig:1DIsing}(b), $s''_{i}$ with coupling related to $K''$. Use the expression you had of $x$ to describe qualitatively how does $x=x_{int}$ changes as you perform this partial summation scheme after several times. (Hint: Does it grows to infinite or does it decay to zero or does it fix at certain value?)
	
	6. How would you interpret the behavior you found in the last question? (Hint: The only dimensionless parameter in the system is $K=\frac{J}{k_BT}$, does it goes toward $T=0$ limit or $T=\infty$ limit?)

```
