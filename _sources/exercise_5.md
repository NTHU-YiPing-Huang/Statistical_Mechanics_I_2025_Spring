# Exercise 5

```{admonition} Problem 1: The Debye model
:name: Prob_5-1
:class: tip

In the material when acoustic phonon modes with $|\boldsymbol{k}|\approx 0$, the dispersion of phonon can be simplified as $\omega=c|\boldsymbol{k}|$.  Consider a system with $N$ atoms in a piece of material with system volume $V=L\times L\times L$. Each atom is arranged in a cubic lattice with shortest distance between two atoms to be $a$. Usually, $a$ is called the lattice constant.

1. At every wave vector $\boldsymbol{k}=\frac{2\pi}{L}(l_x,l_y,l_z)$, there are three possible polarization $\alpha=x,y,z$. Each wave vector corresponds to a simple harmonic oscillator mode with characteristic frequency $\omega(\boldsymbol{k},\alpha)=c|\boldsymbol{k}|$. What is the energy spectrum for the simple harmonic oscillator? Using $n(\boldsymbol{k},\alpha)$ to represent the quantum number of the oscillator.
2. What is the partition function, $Z_{\boldsymbol{k},\alpha}$, of this single mode simple harmonic oscillator?
3. If we treat those oscillators as independent oscillators, they are statistically independent. As we learned in the canonical ensemble approach to the ideal gas model, we can construct the total partition function by forming a product of those independent partition functions for each modes.

$$
	Z=\prod_{\{\boldsymbol{k},\alpha\}}Z_{\boldsymbol{k},\alpha}
$$
Derive the expression of $\ln Z$.
4. For large system $L\gg a$, we can replace the discrete summation over $\boldsymbol{k}$ by continuous integral, $\sum_{\boldsymbol{k}}\to \left( \frac{1}{\Delta k} \right)^3\int d^{3}\boldsymbol{k}$. Assuming the continuous system is isotropic, we can replace the $d^{3}\boldsymbol{k}$ by $4\pi k^2dk$. Construct the function $\ln Z$ following above simplification.
5. One key step of Debye model is to introduce a wave vector cutoff $k_{D}$ according to the total number of atoms by 

$$
	\sum_{|\boldsymbol{k}|\le k_{D}}\approx \frac{V}{(2\pi)^3}\int_{0}^{k_D}4\pi k^2dk=N
$$
Use this expression to derive the expression of $\ln Z$ and E. Show the result using $N k_B$ and $\hbar \omega_{D}$ as parameters. Here $\hbar \omega_{D}=\hbar c k_{D}$.
6. Derive the expression for specific heat and express the result using $k_BT_D$, here $k_BT_D=\hbar\omega_D$.
7. The specific heat has asymptotic behavior at $T\gg T_D$ and $T\ll T_{D}$. Show your calculation and discuss how the specific heat of Debye model depends on the temperature $T$ at the two limits.
```

```{admonition} Problem 2: The grand canonical ensemble for Boson and Fermion Gases
:name: Prob_5-2
:class: tip

The free boson or fermion can be described by the grand canonical ensemble as 

$$
	\ln Z_{GC}=(2S+1)\frac{V}{h^3}\int d^{3}\boldsymbol{p}\ln \zeta_{\pm}\left(\frac{p^2}{2m}-\mu\right)=(\pm)(2S+1)\frac{V}{h^3}\int_{0}^{\infty}4\pi p^2dp\ln \left[ 1\pm z e^{-\frac{p^2}{2mk_BT}} \right]\text{.}
$$
Here $S$ represent the magnitude of the spin, $z=e^{\frac{\mu}{k_BT}}$. The sign choice of $+/-$ corresponds to bosonic/fermionic systems.

1. Using the dimensionless variable $q=\frac{p}{\sqrt{2mk_BT}}$, to rewrite the expression of $\ln Z_{GC}$. Show 

$$
	\ln Z_{GC}=(\pm)\left( 2S+1 \right)\frac{V}{h^3}4\pi\left( 2mk_BT \right)^{\frac{3}{2}}\int_{0}^{\infty} q^2\ln\left( 1\pm z e^{-q^2} \right) dq\text{.}
$$
2. Using the expression $\ln\left( 1\pm x \right)=-\sum_{n=1}^{\infty} \frac{\left( \mp x \right)^n}{n}$ to expand the above expression and perform the Gaussian integral exactly. Show

$$
	\ln Z_{GC}=\left( \mp \right)(2S+1)\frac{V}{\lambda^3}\phi_{\frac{5}{2}}(\mp z)\text{,}
$$
here $\lambda=\sqrt{\frac{h^2}{2\pi mk_BT}}$ and $\phi_{\alpha}(z)=\sum_{n=1}^{\infty}\frac{z^{n}}{n^{\alpha}}$ is the polylog function.
3. Calculate the average number of particles using $N=z\frac{\partial \ln Z_{GC}}{\partial z}$ and show

$$
	N=\frac{V}{\lambda^3}(2S+1)(\mp)\phi_{\frac{3}{2}}(\mp z)\text{.}
$$

```

```{admonition} Problem 3: Bosons in Harmonic traps
:name: Prob_5-3
:class: tip

Let us consider a particle in the anisotropic harmonic-oscillaotr potential $V(\boldsymbol{r})=\frac{1}{2}\left( K_x x^2+K_y y^2+K_z z^2 \right)$. Therefore, we can consider the system as three independent harmonic oscillators in three different directions $x,y$ and $z$. The corresponding energy levels can be parameterized by three non negative integers $(n_x,n_y,n_z)$ as

$$
	E(n_x,n_y,n_z)=\left( n_x+\frac{1}{2} \right)\hbar \omega_x+
\left( n_y+\frac{1}{2} \right)\hbar \omega_y+
\left( n_z+\frac{1}{2} \right)\hbar \omega_z\text{.}
$$

1. Let us consider $n_i$ are continuous variables and neglect the zero-point energies (The $\frac{1}{2}\hbar \omega_i$ in $E(n_x,n_y,n_z)$.), we can simplify the energy as $E\approx \varepsilon_x+\varepsilon_y+\varepsilon_z$ where $\varepsilon_i=n_i\hbar \omega_i$. If we define $G(E)$ as the number of states below energy a specific energy $E$. Derive the expression of $G(E)$ in terms of $E$, $\omega_x,\omega_y,\omega_z$ and $\hbar$. (Hint: There are several way to derive this result. One approach is to consider the  problem in the $(n_x,n_y,n_z)$ space. What is the geometric meaning of the states below energy $E$?)
2. Another way to understand density of state is $g(E)=\frac{d G(E)}{d E}$. Using above expression to get the density of states.
3. We also know from the lecture, we can evaluate the particles in the excited statesusing 

$$
	N_{ex}=\int_{0}^{\infty}dE g(E) \frac{1}{e^{E/k_BT}-1}\text{.}
$$
Here, we assume $N_{ex}$ reaches its maximum for $\mu=0$. The definition of the transition temperature, $T_c$, of Bose-Einstein condensation is when the total number of particles can be just accommodated in excited states. That is,
	
$$
	N=N_{ex}(T=T_c,\mu=0)=\int_{0}^{\infty}dE g(E) \frac{1}{e^{E/k_BT}-1}\text{.}
$$
$\int_{0}^{\infty} dx \frac{x^{\alpha-1}}{e^{x}-1}=\Gamma(\alpha)\zeta(\alpha)$. Here, $\zeta(\alpha)=\sum_{n=1}^{\infty}n^{-\alpha}$ is the Riemann zeta function and $\Gamma(\alpha)$ is the gamma function. 
Derive the transition temperature of this system and express the result using $N, \omega_x,\omega_y,\omega_z$ and the Riemann zeta function.
\end{enumerate}

```
