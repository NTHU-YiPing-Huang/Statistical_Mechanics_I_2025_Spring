(Exercise_1)=
# Exercise 1

```{admonition} Problem 1 (Some Gaussian integrals)
:name: Prob_1-1
:class: tip

1. Evaluate the simple generalization of the Gaussian integral we discussed in the lecture.
   
	$$	
		\int_{-\infty}^{\infty}e^{-ax^2+bx}dx=?
	$$
	
2. A $N$ dimensional Gaussian integral is defined as
   
   $$
		\int_{-\infty}^{\infty}dx_1
		\int_{-\infty}^{\infty}dx_2
		\cdots
		\int_{-\infty}^{\infty}dx_N
		\exp\left[ -\frac{1}{2}\sum_{i,j=1}^{N} x_i A_{ij} x_j+\sum_{i=1}^{N} b_ix_i \right]
   $$
	Derive the final expression of this integral using the matrix $A$ and the vector $b$. Here we assume the matrix $A$ is diagonalizable with positive eigenvalues.
3. Fourier transform for Gaussian--
   
   $$
		G(x,t)=\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{ikx}e^{-Dk^2t}dk
$$
	Evaluate this integral by complete the square of the exponent and change the complex integration contour correspondingly.
	One should find the result that $G(x,t)=\frac{1}{\sqrt{4\pi Dt}}e^{-x^2/(4Dt)}$.

```


```{admonition} Problem 2 (Experiment for central limit theorem)
:name: Prob_1-2
:class: tip

Before we proof the central limit theorem, let's try to do a simple numerical experiment. Consider a random variable $X$ with probability distribution function $P(X)$. In general, we require $P(X)$ having a well defined mean and variance. However, to construct a simplest nontrivial mathematical experiment. Let's take $P(X)$ to be a box distribution ranging from $-1$ to $1$. That is, $P(X)=\frac{1}{2}$ if $X\in[-1,1]$, else $P(X)=0$. The distribution obviously have a well defined mean and variance (Why? Convince yourself it's true). Now, lets try to calculate the following quantity and plot it's distribution function with the Gaussian function with the same variance.

1. Distribution function of the sum of two random variables: $S_2=X_1+X_2$, with $X_1$ and $X_2$ from $P(X)$. Find $P(S_2)$, evaluate the variance of $S_2$ and plot $P(S_2)$ and the Gaussian with the same mean and variance on the same graph. 

2. Distribution function of the sum of three random variables: $S_3=X_1+X_2+X_3$, with $X_1$, $X_2$ and $X_3$ from $P(X)$. Find $P(S_3)$, evaluate the variance of $S_3$ and plot $P(S_3)$ and the Gaussian with the same mean and variance on the same graph. 

Please notice how fast the sum $S_N$ approaches a Gaussian distribution.

```


```{admonition} Problem 3 (Universal behavior of the sum of random variables-- The central limit theorem)
:name: Prob_1-3
:class: tip

Consider independent random variables $\left\{ x_j \right\}$ with a single variable distribution function $P_1(x_j)$. We want to understand the distribution function of the sum of the random variables. That is, we want to derive the distribution function of $X\equiv\sum_{j=1}^{N}x_j$. We are interested in the case where $N$ is large. We can formally write it as

$$
	P_N(X)=\int_{-\infty}^{\infty}d{x_1}\dots \int_{-\infty}^{\infty}d{x_N} P_1(x_1)P_1(x_2)\dots P_1(x_N) \delta(x_1+x_2+\dots+x_N-X).
$$

Here $\delta(x)$ is the Dirac delta function. The Fourier transform of the distribution function is

$$
	\widetilde{P_N}(k)&= \int_{-\infty}^{\infty}dX e^{-ikX}\left[ \int_{-\infty}^{\infty}d{x_1}\dots \int_{-\infty}^{\infty}d{x_N} P_1(x_1)P_1(x_2)\dots P_1(x_N) \delta(x_1+x_2+\dots+x_N-X) \right]\nonumber\\
		&= \left[ \widetilde{P_1}(k) \right]^N
$$
	
, here

$$
	\widetilde{P_1}(k)=\int_{-\infty}^{\infty}dx P_1(x)e^{-ikx}=\langle e^{-ikx}\rangle.
$$

We can consider $\widetilde{P_1}(k)$ as the Fourier transform of $P_1(x)$. Or, we can consider it as the average of $e^{-ikx}$ with respect to the distribution function $P_1(x)$. In the following, we will consider the second interpretation. Expand the exponential, we will have

$$
	\langle e^{-ikx}\rangle =1-ik\langle x\rangle +\frac{(-ik)^2}{2!}\langle x^2\rangle +\frac{(-ik)^3}{3!}\langle x^3\rangle +\dots.
$$

We would like to approximate $\widetilde{P}_1(k)$ as $\widetilde{P}_1(k)\approx e^{f(k)}$. This expression will be useful since we can express $P_N(X)=\frac{1}{2\pi}\int_{-\infty}^{\infty}\left[ \widetilde{P}_1(k) \right]^N e^{ikX}dk=\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{N f(k)} e^{ikX}dk$. We know how to perform this type of integral at least to quadratic power of $k$. (With a simple change of variable, the integral to quadratic order in $k$ is identical with the problem 1.)
So our next goal is to find $f(k)$ in the expression $\widetilde{P}_1(k)\approx e^{f(k)}$.

1. Use the Taylor expansion of $\ln(1+x)=x-\frac{x^2}{2}+\frac{x^3}{3}+\mathcal{O}(x^4)$, we can express $\ln \widetilde{P}_1(k)=\ln \left[ 1-ik\langle x\rangle +\frac{(-ik)^2}{2!}\langle x^2\rangle +\frac{(-ik)^3}{3!}\langle x^3\rangle +\dots \right]$ in powers of $k$. Then we can exponentiate this expression to get $f(k)$. Find the expression of $f(k,k^2,k^3)$ to the third order in $k$. (Hint: your result will looks like $f(k)\approx C_1 k+ C_2 k^2+C_3 k^3+\dots$, find $C_1,C_2,C_3$ as a function of $\langle x\rangle ,\langle x^2\rangle ,\langle x^3\rangle $.

2. Then, we can formally express $P_N(X)$ as

$$
	P_N(X)\approx \frac{1}{2\pi}\int_{-\infty}^{\infty}e^{N(C_1k+C_2k^2)} e^{ikX}\left[ 1+C_3k^3+\dots \right]dk
$$

by expanding the exponent with $C_3k^3$.
We can use the following trick to express this integral in another form. In $\left[ 1+C_3k^3+\dots \right]$ expression, we can replace $(ik)\leftrightarrow \frac{\partial}{\partial X}$ simply because 

$$
	\frac{\partial^m}{\partial X^{m}}\left[ e^{N(C_1k+C_2k^2)} e^{ikX} \right]=\left[ e^{N(C_1k+C_2k^2)} e^{ikX} \right](ik)^{m}.
$$

Therefore, we have

$$
	P_N(X)&\approx\frac{1}{2\pi} \int_{-\infty}^{\infty}e^{N(C_1k+C_2k^2)} e^{ikX}\left[ 1+C_3k^3+\dots \right]dk\nonumber\\
	&= \left[ 1+iC_3\left( \frac{\partial^3}{\partial X^3} \right)^3+\dots \right]\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{N(C_1k+C_2k^2)} e^{ikX} dk
$$

As mentioned before, the last integral is a Gaussian integral that we know how to perform. Complete the square and derive the result of $P_N(X)$ to leading order (ignoring the $iC_3\left( \frac{\partial^3}{\partial X^3} \right)^3$ term and beyond.). (Furthermore, you can ask: how the higher-order correction scales as a function of $N$, but this will be left as a challenge that is beyond this homework problem.)
		
3. After we answered the above questions, we basically derived the *central limit theorem*. That is, the distribution function for the sum of random variables from a distribution function $P_1(x)$ is a Gaussian. That is a very general result. What conditions does $P_1(x)$ need to satisfy to apply the central limit theorem? Will it work when $P_1(x)$ is a Gaussian distribution? Will it work when $P_1(x)$ is a Cauchy distribution?


```


```{admonition} Problem 4 (Freely Jointed Chain--Gaussian model)
:name: Prob_1-4
:class: tip

Polymers are large(high molar mass) molecules composed of a large number of monomers bonded together to form a chain. In reality, the monomers are bounded covalently. That is, the potential energy between two monomers should be a complex function of the bonding angle between two nearby monomers. Let's make some assumptions to simplify our problem which leads to the freely jointed model. (We might over simplify the problem but let's just try it first to get a feeling about what kind of problem we are facing. Then we can ask how to put back more ingredients to make our analysis more realistic.)
	
* We assume the joint of the monomers can rotate freely, \emph{i.e.} the potential energy is independent of the bonding angle, $\phi$, between two nearby monomers. 
* We assume the monomers can overlap with each other in space and have no interaction between each other.
	The model with above two assumptions is the freely jointed chain model. It is the idealization of polymers analogous to ideal gas model for gases.

	```{figure} /images/polymers.pdf
	---
	width: 750px
	name: polymers-fig
	---
	Schematic picture of a single chain polymer molecular formed by the monomers represented by the grey oval.
	```
A key property that we are interested in is the size of the polymer. Usually the polymer coils up. The way they coils up will be a competition between the entropy and the energetics.  Therefore, the size of the polymer is not simply the number of monomers, $N$, times the size of the monomer, $a$. Instead, we need to use some statistical description to characterize the size of the polymer.  Usually, we use the root-mean-square end-to-end distance, $\langle r^2\rangle ^{1/2}$, as a measure for the size of the polymer. Here, $r$ is the distance from one end of the polymer to the other in three-dimensional space. The average is taken over all possible ways the polymer coils. One of the configuration is simple, if all the monomers are aligned in one direction, the end-to-end distance $r_{straight}=Na$. However, this is just one of the possible value of $r$, once the polymer coils, $\langle r^2\rangle ^{1/2}<Na$	
1. It is interesting to observe that the freely jointed model in one-dimension is actually the simple one-dimensional random walk we discussed during the lecture. The step size is just the size of the monomer. The one-dimensional constraint restricts $\phi=0/\pi$. Let's start in this simple limit and use $x$ to represent the end-to-end distance in one-dimensional case. Derive the probability distribution $P_{1D}(x,N)$ when the number of monomers $N$ is large.
2. For the three-dimensional case, we assume the orientation is completely random and the vector from monomer $i$ and the vector for monomer $i+1$ are uncorrelated. \emph{i.e.} $\langle \boldsymbol{d}_{i}\cdot \boldsymbol{d}_{j}\rangle_{i\neq j}=0$. Therefore, we expect $N$ to be distributed evenly $N_{x}=N_{y}=N_{z}=\frac{N}{3}$. Here, $N_{x}$ is a rough definition of the monomer belongs to the monomer in $x$ direction. We can simply consider the projection of the monomer to the $x,y,z$ direction. If the projection to $x$ direction is has the largest size, we said it is a $x$ monomer that should be counted in $N_x$. Derive $\langle r^2\rangle ^{\frac{1}{2}}$ and express it using $N$ and $a$. This is a simple estimation for the size of the polymer. (Sometimes you will see people use the radius of gyration $r_{g}^2$ to estimate the size of the polymer. $r_g$ is the average distance between monomers and the center of mass. It turns out the length scale, $\langle r_g^2\rangle $, will be proportional with $\langle r^2\rangle $. We will not discuss the calculation here, but just mention the fact that using the root mean square of the end-to-end distance capture the essential information for the size of the polymer.)

```
