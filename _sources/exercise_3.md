# Exercise 3

```{admonition} Problem 1: Generalization of the concept of phase space in a quantum system
:name: Prob_3-1
:class: tip

The uncertainty principle of quantum mechanics provides a fundamental unit of the phase space volume. Please read the chapter 3.5 of Peliti's textbook about the quantum states and the example to evaluate the occupied phase space by a quantum state using the simple harmonic oscillator. In this problem, we will use another example to check whether we really understand the idea.
Consider a quantum particle of mass $m$ moving in one dimension along a line of length $L$.

1. Show the possible energy values to be $E_n=\frac{\hbar^2\pi^2n^2}{2mL^2}$ where $n=1,2,\dots$.
2. Prove the phase space volume occupied by each quantum state is equal to $h$.
```

```{admonition} Problem 2: *Phase space* : Explain your answer concisely using 3 to 5 sentences.
:name: Prob_3-2
:class: tip

Consider two microscopic states of the same system described by $\xi_{1}(t)$ and $\xi_{2}(t)$. Here, $\xi_i(t)$ is a point in the phase space at time $t$ where $i=1,2$. As time evolves, $\xi_i(t)$ form a path in the phase space. 

1. Can the path $\xi_{1}(t)$ and $\xi_{2}(t)$ intersects with each other under canonical evolution (energy is conserved)?
2. If the energy is not conserved (dissipative force exists), is it possible that the two path ends up at the same point in the phase space? 

Explain why you got this answer or give a simple example to demonstrate your point.
```

```{admonition} Problem 3: Some properties of entropy following Boltzmann's postulate
:name: Prob_3-3
:class: tip

During the lecture, we introduce Boltzmann's postulate

$$
	S=k_B\ln(|\Gamma|)
$$

We want to check whether this new definition fits our understanding of the thermodynamic entropy $S$.

1. Thermodynamic entropy is an extensive quantity: 
	
	1. (Isolated systems): Consider isolated system $A$ and system $B$. The microscopic configurations in the phase space of $A$ and $B$ can be represented by two $\xi_A \in \Gamma_A$ and $\xi_B \in \Gamma_B$ where $\Gamma_A,\Gamma_B$ represent the phase space of the two systems. Since $A$ and $B$ are both isolated, the microscopic configurations of the composite system $A\cup B$ can be described as $\xi^{(A\cup B)}=\{\xi_A,\xi_B\}$. Using this simple setting, calculate the phase space volume of the composite system $A\cup B$ (represent you answers by $\Gamma_A$ and $\Gamma_B$.) and show that the thermodynamic entropy following Boltzmann's definition is an extensive quantity.
	2. (Systems in thermal contact): Consider the two system $A$ and $B$ can exchange energy with each other, but they are isolated from the rest of the world. Therefore, the total energy $E^{(A)}+E^{(B)}=E^{(A|B)}=E$ is kept fixed. Here we use $(A|B)$ to represent the composite system which is the two systems in thermal contact.
	The phase space of the composite system is
	
	$$
		|\Gamma_{(A|B)}|=\sum_{E^{(A)}}|\Gamma^{(A)}(E^{(A)})||\Gamma^{(B)}(E-E^{(A)})|\text{.}
	$$				
	Here, we can assume energy is a continuous variable and approximate the above summation using integral representation, *i.e.*
	
	$$
	|\Gamma_{(A|B)}|\approx \int \frac{dE^{(A)}}{\Delta E^{(A)}} \exp\left[ \frac{1}{k_B}\left( S_{A}(E^{(A)})+S_{B}(E-E^{(A)}) \right) \right]\text{.}
		\label{int_rep}
	$$
	* Convince yourself that this is how things should be when you calculate the phase space of the composite system. After some time, the system reaches equilibrium, so the energy configuration will becomes $E^{(A)}_{eq}+E^{(B)}_{eq}=E$. Notice the fact that the equilibrium configuration will contribute $|\Gamma_{(A|B)_{eq}}|$, which is just one part of the total phase space $|\Gamma_{(A|B)}|$. Expand $E^{(A)}$ in the integral of Eq. (\ref{int_rep}) near the equilibrium configuration $E^{(A)}_{eq}$ up to quadratic order in $(E^{(A)}-E^{(A)}_{eq})$, you will have an expression looks like Gaussian integral. Once you perform the Gaussian integral, you should have
		
		$$	
			|\Gamma_{(A|B)}|\approx |\Gamma_{(A|B)_{eq}}| \times (\text{contribution from the Gaussian integral})\text{.}
		$$
		Identify the system size dependence of the contribution from the Gaussian integral. (Basically, how it depends on $N$ when $N$ is large)
	* In the above derivation, we use $|\Gamma^{(\mu)}(E^{(\mu)})|=\exp\left[ \frac{S_{\mu}(E^{(\mu)})}{k_B} \right]$  with $\mu=A/B$ to express the phase space of individual system initially. After we derive the approximated phase space volume $|\Gamma_{(A|B)}|$, we should be able to evaluate $S_{(A|B)}$ and express it using $S_{A}(E^{(A)}_{eq})$ and $S_{B}(E^{(B)}_{eq})$. Find the difference between $S_{(A|B)}$ and $S^{(A\cup B)}_{eq}\equiv S_{A}(E^{(A)}_{eq})+S_{B}(E^{(B)}_{eq})$. Will this difference be important when $N\to\infty$? If the contribution of this difference is sub-leading in $N$ as $N\to\infty$, we establish the relation that $S_{(A|B)}\approx S^{(A\cup B)}_{eq}= S_{A}(E^{(A)}_{eq})+S_{B}(E^{(B)}_{eq})$.

```

```{admonition} Problem 4: Microcanonical ensemble
:name: Prob_3-4
:class: tip

Ising model is a simplification for the real magnetic system. The magnetic moment is assumed to have fixed value and can only take two possible orientation opposite with each other. For the $i$-th magnetic ion, the magnetic moment is represented by $\boldsymbol{\mu}_i=\mu \sigma_i$. Here, $\mu$ is the magnitude of the moment and $\sigma_i=\pm1$. The spins in the paramagnetic phase are statistically independent from each other. Then, we ask the question: given specific $M$ value, what is the accessible phase space of the system? Basically, we can randomly pick some spins to point up and some spins to point down as long as the value of $M$ corresponding to the specified value. So the accessible phase space volume is

$$
	|\Gamma|=\frac{N!}{\left[\frac{1}{2}\left( N+\frac{M}{\mu} \right)\right]!\left[\frac{1}{2}\left( N-\frac{M}{\mu} \right)\right]!}\text{.}
$$

1. From the expression, we can derive $S(M)$ explicitly through the Stirling's approximation. (Assuming $N$, $M$ are macroscopic quantities.) Derive $S(M)$ after using the Stirling's approximation.
2. Use the result of $S(M)$ to find the equation of state $m\equiv \frac{M}{N}=\mu \tanh \left( \frac{\mu h}{k_BT} \right)$. (Hint: you can use the identity $\frac{1}{2}\ln\frac{1+x}{1-x}=\tanh^{-1}x, |x|<1$.)
3. The constant field specific heat is defined as $C_h=\left.T\frac{\partial S}{\partial T}\right|_{h}$. Find the expression of $C_h$.

```

```{admonition} Problem 5: Canonical ensemble at fixed temperature $T$
:name: Prob_3-5
:class: tip

1. Single spin case:
	1. Consider an Ising spin with $\mu=1$ with proper unit, $\sigma_1=+1$ or $-1$, in the external field, $h$. The energy of this  system is $H_1=-h\sigma_1$. What are the possible energies of this system? What are the microscopic configurations of the Ising spin for the corresponding energies?
	2. Write down the partition function $Z_1$ of this single spin system.
2. Three spins case:
	1. Consider three such Ising spins decoupled from each other. That is, the total energy of the three spin system is $H=-h(\sigma_1+\sigma_2+\sigma_3)$. What are the possible microscopic configuration of the spins? You can imagine the spins are sitting at real space, so they are distinguishable according to their coordinates. What are the corresponding energies for each configuration?
	2. Write down the partition function $Z$ of this three-spin system.
3. Show that $Z=(Z_1)(Z_2)(Z_3)=(Z_1)^3$. Here $Z_i$ is the partition function of the $i$-th spin.
4. Suppose the Ising spin $\sigma_1$ does not like to align with spin $\sigma_2$, usually it means the system pays more energy to aligning the direction of $\sigma_1$ and $\sigma_2$. We can describe such effect by including a term $J\sigma_1\sigma_2$ with $J>0$. That is, the total energy is now described by $H'=-h\left( \sigma_1+\sigma_2+\sigma_3 \right)+J\sigma_1\sigma_2$. We can construct the corresponding partition function $Z'$ accordingly. Do you expect to have a factorizable structure as $Z'=(Z_1')(Z_2')(Z_3')$?  Why? or Why not? Here $Z_i'$ is the partition function formed by the degree of freedom $\sigma_i$.

```

```{admonition} Problem 6: Estimate the probability of electrons at the ground state of Hydrogen atom:
:name: Prob_3-6
:class: tip

We can use what we have learned during statistical mechanics to understand some systems we have learned. One important system is the Hydrogen atom, the electron has discrete energy levels with $E_n=-\frac{E^{*}}{n^2}$. Here, $E^{*}=13.6 eV$ and $n$ is the principle quantum number. Using Bohr model, we have the radius of atom to be $r_{n}=n^2 r_1$, $r_1\approx 5\times 10^{-11}m$. $k_B\approx 8.6\times 10^{-5}eV/K=1.38\times 10^{-23}J/K$.

1. Write down the expression of partition function of the electron , $Z_{e}$, on a Hydrogen atom in the canonical ensemble at temperature $T$. In principle, we should sum all the contribution to $n\to \infty$, the probability of the electron to be at ground state of a Hydrogen atom is $P^{*}=\frac{e^{\frac{E^*}{k_BT}}}{Z_e}$. What is $P^{*}$ when we including all states $E_n$? Does it make sense?
2. The mean free path, $l$, of molecular in the air at ambient pressure at $T=$300K is around $7\times 10^{-8}$m. Which means the distance between two collision event is about $l$. If we use the expression of $r_n$ above, what is the minimal value $n_l$ such that $r_{n_l}> l$?
3. The thermal wave length at temperature $T$ is $\lambda_T=\left( \frac{h^2}{2\pi m k_B T} \right)^{1/2}$. The mass of hydrogen atom is about $1.66\times 10^{-27}kg$. What is the thermal wave length for a Hydrogen atom at $T=300K$?  What is the minimal value  $n_{T}$ such that $r_{n_T}>\lambda_{T}$?
4. You can use $n_l$ or $n_{T}$ to cutoff your expression in $Z_e$, write down the formal expression of the partition function and the corresponding $P^{*}$ as a function of the cutoff. For the two different cutoff scheme ($n_l$ and $n_{T}$), which one has higher probability $P^{*}$? The evaluation of $P^{*}$ can be done numerically and the two cutoff scheme can give you an estimation of the range of probability $P^{*}$.

```
