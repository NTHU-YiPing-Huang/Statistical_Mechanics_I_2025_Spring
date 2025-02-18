# Density operator formalism 

Here we give a brief review of the density operator fromalism invented by J. von Neumann in 1927. In statistical mechanics, we discuss how to assign probability to the microscopic configuration of our system. Here the probability is a classical probability given by the ensemble theory. On the otherhand, when we are studying quantum system, the quantum mechanics has a build in probability description which should be distinct with the probability given by the ensemble theory. The quantum mechanics probability description is build on top of the interpretation of wave function. The density operator neatly encapsulates the two concepts in a compact and clear framework.

The density operator is defined as

$$
\hat{\rho}=\sum_j P_j|\psi_j\rangle\langle \psi_j|\text{.}
$$

Here, $P_j$ is the probability, given from the ensemble theory, of having a microscopic configuration described by a many-body wave function $|\psi_j\rangle$. $|\psi_j\rangle$ is the many-body wave function that takes care of the quantum part of the probability interpretation. In general, $|\psi_j\rangle$ need not be orthogonal. A well defined density operator provides the following information:

1. The set of possible states $|\psi_j\rangle$.
2. The classical probability, $P_j$, for the ensemble to have state $|\psi_j\rangle$.

Let's understand the density operator bits by bits. If we call an ensemble with only one possible state $|\psi_p\rangle$ a pure ensemble (The simplest case!). The density operator for the pure ensemble with wave function (In general, the wave function need not be a many-body wave function, for this lecture, we usually will care about the many-body wave function.) $|\psi_p\rangle$ will simply be

$$
\hat{\rho}_p=\sum_j \delta_{p,j}|\psi_j\rangle\langle\psi_j|=|\psi_p\rangle\langle \psi_p|\text{.}
$$

If we represent the operator $\hat{\rho}_p$ in some complete basis, $|\alpha_m\rangle$, given by observable $\hat{A}$. We will have

$$
\left(\hat{\rho}_p\right)_{\alpha_m,\alpha_n}=\langle \alpha_m|\hat{\rho}_p|\alpha_n\rangle=\left(c^{(p)}_{\alpha_m}\right)^*c^{(p)}_{\alpha_n}\text{.}
$$
The normalization condition of $|\psi_p\rangle$ suggests $Tr[\hat{\rho}_p]=\sum_{m}|c^{(p)}_{\alpha_m}|^2=1$.

The ensemble with more than one possible states is called a mixed ensemble, it can be understood as a collection of pure ensembles with specified probability. The wave function normalization condition plus the normalization of the probability assignment gives

$$
\sum_j P_j\underbrace{\sum_m \langle \alpha_m|\hat{\rho}_j|\alpha_m\rangle}_{=1}=\sum_j\sum_m P_j|c^{(j)}_{\alpha_m}|^2=Tr[\hat{\rho}]=1\text{.}
$$
In the above expression, I explicitly show the structure of $P_j|c^{(j)}_{\alpha_m}|^2$. That simply means: the probability for our mixed ensemble to have observable $\hat{A}$ with measured value of $\alpha_m$ is the product of classical probability $P_j$, the chances that the state we pick from the mixed ensemble to be $|\psi_j\rangle$, times the quantum probability $|c^{(j)}_{\alpha_m}|^2$, the probability that the system collapes from $|\psi_j\rangle$ to $|\alpha_m\rangle$ after the measurement. The diagonal terms basically contains those information.

We can next consider the off-diagonal terms of density operators.

