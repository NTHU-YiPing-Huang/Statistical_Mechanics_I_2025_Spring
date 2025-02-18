# Exercise 4

```{admonition} Problem 1: Simplest application of duality-- factorization of partition function
:name: Prob_4-1
:class: tip

In our previous homework, we have shown that non-interacting system has a nice property that the partition function factorizes. The reason is the total energy of the system is just the sum of the energy of individual sub-components. We also realize that if there is energy stored between different sub-components, it kind of suggest that we cannot factorize the partition function. (But, is it always true?) Let's try to revisit the issue again here using the Ising model.
The Ising model for $N$ spins without external field can be described as

$$
	H=-J\sum_{i=1}^{N-1}\sigma_i\sigma_{i+1}\text{.}
$$
Here, we assume the system has open boundary condition. $\sigma_{i}=\pm1$ is the Ising variable.

1. Let's start from a small system with $N=3$. Write down the possible configurations for the system and the corresponding total energy.
2. What's the canonical partition function, $Z_{N=3}$, for the $N=3$ system at temperature $T$?
3. Can you factorize $Z_{N=3}$ in some way such that $Z_{N=3}=K(\mathcal{Z})^2$? Here, $K$ is a numerical factor.
4. If you interpret $\mathcal{Z}$ as a partition function, what the corresponding energy means in the original model? What is the meaning of $K$?
5. Let's relax the $N=3$ condition, what is the partition function for arbitrary $N$? The line of thought here is sometimes referred as \emph{duality}. Some kind of neat way to perform changes of variable. This is the simplest version of it, but there are more sophisticated and interesting extensions of this idea.
```

```{admonition} Problem 2: A two-level system-- Schottky anomaly
:name: Prob_4-2
:class: tip

Consider $N$ independent two level systems with energy levels $E_1$ and $E_2$ at temperature $T$. We assume $E_2>E_1$ and the energy gap is $\varepsilon=E_2-E_1>0$.

1. Write down the canonical partition function, $Z$, for the $N$ independent two level systems. Express the result using $E_1$ and $\varepsilon$.
2. Derive the expectation value of energy using $E=-\frac{\partial \ln Z}{\partial \beta}$. Here $\beta=\left( k_BT \right)^{-1}$.
3. The specific heat of the system is $C=\frac{\partial E}{\partial T}$. Derive the expression in terms of $\theta=\frac{\varepsilon}{k_BT}$. 
4. Find the asymptotic behavior (to leading order in $\theta$) of $C$ at the following two limits. (i) $k_BT\ll \varepsilon$ and (ii) $k_BT\gg\varepsilon$.

The specific heat will have a maximum value at the temperature such that $k_BT\approx \varepsilon$. That is, one can use the peak of the specific heat to have a rough idea about the energy gap for the two level system. A very useful estimation for the modeling from experiment data!
```

```{admonition} Problem 3: Concept of density of states
:name: Prob_4-3
:class: tip

Another way to express density of states is by $D(E)=\frac{1}{V}\sum_{i=1}^{N}\delta\left( E-E(\boldsymbol{k}_{i}) \right)$ for discrete $\boldsymbol{k}_{i}$. For continuous $\boldsymbol{k}$ in $d$ dimension, we have $D(E)=\frac{1}{L^{d}}\left( \frac{L}{2\pi} \right)^{d}\int d^{d}\boldsymbol{k}\delta(E-E(\boldsymbol{k}))=\int \frac{d^{d}\boldsymbol{k}}{(2\pi)^{d}} \delta(E-E(\boldsymbol{k}))$. (Note: density of states counts the number of states per volume in an energy shell. The value could differ when we use different boundary conditions. Here, we use the hard wall boundary condition with $\phi(0)=\phi(L)=0$. Also, we consider spinless fermions for all questions in this problem. Therefore, we can drop the (2S+1) factor related to the internal degree of freedom.) We also have learned in HW2 that $\int_{-\infty}^{\infty} d^{d}\boldsymbol{k}=\int_{0}^{\infty}S_{d}k^{d-1}dk$ with $S_d=\frac{2\pi^{d/2}}{\Gamma(d/2)}$. $\delta(x^2-a^2)=\frac{1}{2|a|}\left[ \delta(x+a)+\delta(x-a) \right]$, you will use above identity frequently. Consider the following questions

1. Density of states for free particles in a box with at different dimensions, $E=\frac{\hbar^2 |\boldsymbol{k}|^2}{2m}$ and the volume is $L^d$.
	1. For 1D system ,we have $D_{1D}(E)=\int_{-\infty}^{\infty} \frac{d k}{2\pi}\delta(E-\frac{\hbar^2 k^2}{2m})$. Evaluate this integral and get the expression of $D_{1D}(E)$.
	2. Repeat above calculation for the 3D case
	3. Derive the general expression for $d$-dimensional case.
2. Derive the Fermi energy in $d$ dimension for system with $N$ electrons. Express the final result using density at $d$ dimension, $n_d=\frac{N}{L^d}$.
3. Using the general expression of the density of state in $d$ dimension, we can repeat the simple minded guess of the specific heat of degenerate Fermi gas to be $C\approx \frac{D_d(E_F)L^d(k_BT)^2}{T}=D_d(E_F)L^d k_B^2 T$. Show that $C\propto \frac{T}{T_F}$ is independent of dimension.
4. Here is an interesting puzzle to understand the meaning of density of state in 1D.
	From the description of density of state, we know the meaning of density of state is to convert the integral from $d\boldsymbol{k}$ to $dE$. In 1D, $d\boldsymbol{k}$ is almost equivalent to $dk$.
	We can use another way to derive the density of states. First, we have $\frac{d E}{dk}=\frac{\hbar^2 k}{m}$. Then, we replace $k=\sqrt{\frac{2mE}{\hbar^2}}$. So we have $dk=\frac{m}{\hbar \sqrt{2mE}}dE=\frac{1}{2\hbar}\sqrt{\frac{2m}{E}}dE$. If we use the definition that the density of state is the number of state per volume in an energy shell. We should have the density of state by $\frac{1}{L}\frac{dk}{\Delta k}=\frac{1}{2\pi}dk=\frac{1}{2\pi}\frac{1}{2\hbar}\sqrt{\frac{2m}{E}}dE=d(E)dE$. The density of state $d(E)$ derived using this approach is $d(E)=\frac{1}{2\pi}\frac{1}{2\hbar}\sqrt{\frac{2m}{E}}$. Compare $d(E)$ with the $D(E)$ in 1 (a). Did they agree with each other? If not, why the two approaches give different answers?
\end{enumerate}


```
