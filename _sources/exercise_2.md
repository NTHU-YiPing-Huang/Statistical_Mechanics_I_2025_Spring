(Exercise_2)=
# Exercise 2

```{admonition} Problem 1 (Diffusion equation in $d$ dimension)
:name: Prob_2-1
:class: tip

The diffusion equation can be generalized into $d$ dimension as

$$
	\frac{\partial \rho}{\partial t}=D\nabla^2 \rho\text{.}
$$
Here, $\nabla=\left( \frac{\partial}{\partial x_1},\frac{\partial}{\partial x_2},\dots,\frac{\partial}{\partial x_d} \right)$. We consider $t>0$ for our convenience.
As in 1D, we can defined the Green's function $G(\boldsymbol{x},t)$ to be the time evolution of the initial density $G(\boldsymbol{x},0)=\delta(\boldsymbol{x})$ with a particle sits at the origin. $G(\boldsymbol{x},t)$ needs to satisfy the diffusion equation

$$
	\frac{\partial G(\boldsymbol{x},t)}{\partial t}=D\nabla^2 G(\boldsymbol{x},t)\text{.}
$$
Since the diffusion equation in $d$ dimension also has translational symmetry, we can follow the same steps as we did in $d=1$ to derive the Green's function $G(\boldsymbol{x},t)$.
Show your derivation at each step and derive

$$
	G(\boldsymbol{x},t)=\int \frac{d^{d} q}{(2\pi)^{d}}e^{i\boldsymbol{q}\cdot \boldsymbol{x}}\tilde{G}_{\boldsymbol{q}}(t)=\frac{1}{\left( 4\pi D t \right)^{\frac{d}{2}}}e^{-|x|^2/4Dt}\text{.}
$$
```


```{admonition} Problem 2 (Simplified version of random matrix theory)
:name: Prob_2-2
:class: tip

The random matrix theory is invented by Eugene Wigner to describe the spectra of nuclei of heavy atoms. To introduce the topic properly probably requires another year-long course. So we are not going to discuss the details of it. However, the main idea can be demonstrated using $2\times 2$ Hamiltonians. That can be done during a homework problem of statistical mechanics (I).
Consider a set of $2\times 2$ Hamiltonians\,

$$
	\widehat{H}=\left(
	\begin{array}{cc}
		\varepsilon_1 &\frac{V}{\sqrt{2}}\\
		\frac{V^{*}}{\sqrt{2}} &\varepsilon_2
	\end{array}
	\right)\text{.}
$$
One can easily diagonalize the above Hamiltonian and get the eigenvalues as

$$
	E_{1,2}=\frac{\varepsilon_1+\varepsilon_2}{2}\pm\frac{1}{2}\sqrt{\left( \varepsilon_1-\varepsilon_2 \right)^2+2|V|^2}\text{.}
$$
This is the level repulsion physics for a general (no symmetry constraints) $2\times 2$ Hamiltonian.

1. Consider the matrix elements ,$\varepsilon_1$, $\varepsilon_2$ and $V$ are random real numbers extracted from Gaussian distribution with width of the distribution to be $\sigma$. The statistics of the level separations $P(E_1-E_2=\omega)\equiv P(\omega)$ can be expressed as

	$$
		P(\omega)=\frac{1}{(2\pi)^{3/2}\sigma^3}\int d\varepsilon_1 \int d\varepsilon_2\int dV\delta\left( \sqrt{(\varepsilon_1-\varepsilon_2)^2+2V^2}-\omega \right) \exp\left[ -\frac{\varepsilon_1^2+\varepsilon_2^2+V^2}{2\sigma^2} \right]\text{.}
	$$
What is $P(\omega)$?
(*Hint: Evaluate this integral by change of variable $\varepsilon_2=\varepsilon_1+\sqrt{2}\xi$ and integrate $\varepsilon_1$. After that, $\varepsilon_2$ and $V$ will look symmetric, one can use the polar coordinates to simplify the integral further and get the result.*)
2. Now let's consider $V$ to be complex in general. That means both the real part and the imaginary part of $V$ are random. Consider the real part and imaginary part are also random numbers extracted from Gaussian distribution functions with width $\sigma$ and repeat the calculation in the previous question. Find $P(\omega)$ in this case.

The random matrix theory is initially invented for the spectra of nuclei of heavy atoms initially. However, it becomes one of the key concept to explore the physics of thermalization which is an important problem in the past decade or so in quantum statistical mechanics.

```

```{admonition} Problem 3 (Why large $N$ is useful? Properties of $N$-dimensional space:)
:name: Prob_2-3
:class: tip

In statistical mechanics, we work in the phase space with dimension $N$ to be large. Such space has properties that are very counter intuitive. Since $N$ is large, so we might be able to use it as a big parameter and construct the saddle point approximation (Which is useful to expand our analytic understanding). So we can see the fact that $N$ is large actually simplifies our problem if we use it wisely. We discuss some properties of the $N$-dimensional space.

1. From dimension analysis, we know the volume of a sphere with radius $R$ in $N$ dimension should be proportional with $R^{N}$. Explain why it is so. (Hint: The definition of volume in $N$ dimensional space is $\int \prod_{i=1}^{N}dx_{i}$. One can start from this expression.)
2. Above observation suggests we can define the volume of a sphere with radius $R$ as $\text{Vol}_N(R)=C_N R^{N}$ in $N$ dimension. Suppose we have a sphere with radius $R-\delta R$(with $\delta R\gtrsim0$) which is smaller than $R$. What is the ratio $r_{N}\equiv\frac{\text{Vol}_N(R)-\text{Vol}_N(R-\delta R)}{\text{Vol}_N(R)}$ at the $N\to\infty$ limit? The ratio is the ratio between volume of the thin shell with radius $R$ and the volume of the whole sphere with radius $R$. What is the meaning of your result? (Hint: Before we do any calculation, there could be two possibilities: (1) $\lim_{N\to\infty} r_N\to0$, (2)$\lim_{N\to\infty} r_N\to1$. (1) means the outer shell contributes very little to the total volume. (2) means the outer shell contributes almost 100\% of the total volume. Which case fits your result?)
3. The surface of the sphere with $R$ radius is given by $S_N(R)=\left.S_N(R)\right|_{R=1}R^{N-1}$. Following the steps and show that $S_N(R)=\frac{2\pi^{N/2}}{\Gamma(N/2)}R^{N-1}$. Here, $\Gamma(z)=\int_{0}^{\infty}dt e^{-t}t^{z-1}$ is the Euler Gamma function.
	
	1. Evaluate the $N$ dimensional Gaussian integral.
	
	$$
	G_{N}=\int\prod_{i=1}^{N}dx_{i}exp\left( -\sum_{i=1}^{N}x_i^2 \right)\text{.}
	$$
	2. We can define $a^2=\sum_{i}x_i^2$, and work in the polar coordinate to express $G_N$ as
	
	$$
		G_{N}&=& \int_{0}^{\infty}exp\left( -a^2 \right)S_N(a)da\nonumber\\
		&=&  S_N(1)\int_{0}^{\infty} a^{N-1}exp(-a^2)da\text{.}
	$$
	Using the definition of Euler Gamma function, $\Gamma(z)=\int_{0}^{\infty}dt e^{-t}t^{z-1}$, to derive the expression of $S_{N}(1)$. Show $S_{N}(R)=\frac{2\pi^{N/2}}{\Gamma(N/2)}R^{N-1}$.
2. Using $S_{N}(R)$, we can derive the volume of the $N$ dimensional sphere with radius $R$ as 

	$$
		\text{Vol}_N(R)=C_NR^N\text{.}
	$$ 
	Find the expression of $C_N$.

3. The volume of the $N$ dimensional sphere with radius $R$ can be expressed as 

	$$
		\int\left(\prod_{i=1}^{N}dx_i\right)\theta(R^2-\sum_{j=1}^{N}x_{j}^2)\text{.}
	$$
	The distribution of the sphere's projection onto one of the axes is

	$$
		\rho(x_1)=\int \left(\prod_{i=2}^{N}dx_i\right)\theta\left( R^2-x_1^2-\sum_{j=2}^{N}x_j^2 \right)\text{.}
	$$
	Here, $\theta(x)=1$ if $x\ge0$, otherwise $\theta(x)=0$.

	1. The integral on the right-hand side is the volume of the sphere in $(N-1)$-dimensional space. What is the radius of the $(N-1)$-dimensional sphere? Using the result of previous problems to show $\frac{\rho(x_1)}{R^{N-1}}=C_{N-1} exp\left[ \frac{N-1}{2}\ln[(1-\frac{x_1^2}{R^2})] \right]$.
	2. When $N$ is large, $\frac{\rho(x_1)}{R^{N-1}}$ goes to zero quickly as $x_1$ moves away from zero. Therefore, we can expand the exponent into a Taylor series around $x_1=0$. Perform the Taylor expansion and show $\rho(x_1)$ could be approximate by a Gaussian function as $\frac{\rho(x_1)}{R^{N-1}}\approx C_{N-1}\exp\left[ -\frac{N-1}{2R^2} x_1^2\right]$.

```


```{admonition} Problem 4 (Universality beyond the ideal gas model:)
:name: Prob_2-4
:class: tip

The ideal gas model gives the state equation $P\frac{V}{N}=k_BT$. However, the model is pretty artificial that it consider particles as mathematical points. The Van der Waals equation take into the account that

* The particles are not mathematical points, but with some intrinsic volume. This leads to 

	$$
		P\left( \frac{V}{N}-b \right)=k_BT\text{.}
	$$
* The particles will collide and put pressure on the container. However, the particles will interact(electric dipole, magnetic dipole, \ldots) with each other and modify the expression of pressure. This leads to 

	$$
		\left( P-Q \right)\left( \frac{V}{N}-b \right)=k_BT\text{.}
	$$

	```{figure} /images/VdW.pdf
	---
	width: 750px
	name: VdW-fig
	---
	The toy model for interaction in the Van der Waals model. The dashed lines represent the interaction between the reference particle and its neighbors. (a) represents the case where the reference particle is deep inside the container and cannot see the boundary of the container. (b) represents the case where the reference particle is near the boundary of the container.
	```
	Let's try to use a simple averaged picture to estimate $Q$. The interaction between the particles are complicated. They could depends on the distance between particles as in {numref}`VdW-fig`(a). Let's assume the potential, $U$, describes the interaction between a particle deep inside the container and the rest of the particles near it. And $U_W$ to be the potential when the reference particle is near the wall of the container. From {numref}`VdW-fig`(b), we estimate $U_W=\frac{U}{2}$.

	The density deep inside the container is $\frac{N}{V}$, we expect the density near the wall of the container to be modified. A rough estimation is 

	$$
		\left.\frac{N}{V}\right|_{\text{Wall}}=\frac{N}{V} \mathcal{F}(U_W-U)\xrightarrow{?}\frac{N}{V} exp\left[ -\frac{1}{k_BT}\left( U_{W}-U \right) \right]=\frac{N}{V}exp\left[ \frac{U}{2k_BT} \right]
	$$

	At this point, it is not clear why it is reasonable to estimate the effect of interaction in this way (That is, we don't know where $\mathcal{F}(U_W-U)\approx exp\left[ -\frac{1}{k_BT}\left( U_{W}-U \right) \right]$ came from. It is the Boltzman factor that we will encounter several times later in the lecture. Let's just accept it as a reasonalbe approximation for now.).

	$U$ should be proportional with the density of the system, so we can write $U=\frac{N}{V} u_0$ where $u_{0}=\int_{B(0)}d^{3}\boldsymbol{r} u(r)$. Here we use $B(0)$ to denote the integral region near the reference particle and $u(r)$ is the two particle potential with $r$ denote the distance to the reference particle. Therefore, we have

	$$
		\left.\frac{N}{V}\right|_{\text{Wall}}=\frac{N}{V} exp\left[ \frac{Nu_0}{2Vk_BT} \right]\text{.}
	$$
	When $u_0>0(u_0<0)$, we have a repulsive(attractive) potential between particles. The density near the wall will be larger(smaller) comparing with the density in the bulk.
	Using this picture, it is clear why we have the last equality. Since near the boundary, $U_W$ should only include half of its neighbors, so we have $U_W=U/2$.

1. *Interaction correction to the pressure*: Assume we can apply the ideal gas equation near the wall of the container

	$$
		P=k_BT\left( \left.\frac{N}{V}\right|_{Wall} \right)\text{.}
	$$
	Assume we are still at the dilute gas limit. Find the expression of $P$ to leading order correction in $bN/V\equiv bv^{-1}$ beyond the ideal gas equation by expanding the exponent. With this correction, we can modify the ideal gas model and derive the Van der Waals equation as
	
	$$
		\left( P+\frac{a}{v^2} \right)(v-b)=k_BT\text{.}
	$$
	Derive the expression of $a$ using $u_0$.
2. Expand the Van der Waals equation, one will get a cubic equation $F_{VdW}(v)=0$. The cubic equation has different possibilities of its solution:
	* three real roots of $v$.
	* one real root of $v$ and a pair of complex root of $v$.
	* three degenerate real root $v=v_c$. This corresponds to the \emph{critical point} of the system. 
	Here, we only focus on the last case which corresponds to the case we have $F_{VdW}(v)\propto (v-v_c)^3$. Assuming the corresponding temperature and pressure in this case to be denoted as $T_c$ and $P_c$.
	Find the expression of $T_c,P_c$ and $v_c$ using the parameter $a,b$ in the Van der Waals equation.
3. Show that $\frac{P_c v_c}{k_BT_c}$ is a constant independent of the microscopic detail parameters $a,b$. The meaning of this expression is: for different systems, we will need different microscopic parameter $a$ to describe how they interact and $b$ to describe the correction due to the size of the particles. In general, $a,b$ differs from system to system. However, at the critical point, they all satisfy this relation that the value of the product $\frac{P_c v_c}{k_BT_c}$ is the same constant.
```
