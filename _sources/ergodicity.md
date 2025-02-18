# Ergodicity (Do we really need it?)


Here we will introduce an abstract concept-- ergodicity. The idea provides a connection between time-evolution and the statistical description of the system. However, prove a system is ergodic or not is in general difficult. (That's why I skip the discussion during the lecture. For those who are interested in this concept, please check {cite:p}`sethna2021statistical` {cite:p}`oono2017perspectives` and the related references.) Therefore, the approach is usually we assume our system is ergodic. Then, we argue the **time average** equals **micro canonical averages**. So the idea of ergodicity provides a way to connect the dynamical problem to a statistical problem. 

Actually, we have introduce the concept of microcanonical ensemble even without addressing the ergodicity during the lecture. The reason that we introduce the concept of microcanonical ensemble in that order is to emphasis that there are different ways to formulate statistical mechanics. The route we take during the lecture basically relies on the structure of phase space volume which is a result due to thermodynamics and Boltzmann's postulate.

Once we have establish the microcanonical ensemble, then statistical mechanics can be built on top of it. Statistical mechanics also works phenomenally well. Here, we will have a short discussion about the idea of ergodicity and point out some problems/solutions that we might encountered when establishing statistical mechanics based on ergodicity.

## Ergodicity and ensemble average

Let's first define the notation of time average.
The time average of observable $O$ starting at initial condition $\xi(t=0)$ is

$$
\overline{O(t=0)}\equiv \lim_{T\to\infty} \frac{1}{T}\int_{0}^{T} dt O(\xi(t))\text{.}
$$

Since we are interested in the stationary case, we assume at $T\to\infty$ limit, the system we are interested in reaches a statonary description. In that case, the ensemble average of any physical quanttity $f$ will be independent of time. That is,

$$
\langle f\rangle=\overline{ \langle f\rangle}\text{.}
$$

Since time average and ensemble average are two independent operation, so they commute, we have

$$
\overline{ \langle f\rangle}=\langle \overline{f}\rangle \text{.}
$$

At long-time limit, the time average will be dominated by the stationary contribution. If the system is ergodic, every member of the ensemble will evolved to one another at the $T\to\infty$ limit. Therefore, they are to some extend all equivalent. Also, for every member of the ensemble, they will reach the same long-time average value. Therefore, the ensemble average of the time averaged observable is just average over the same quantity $\overline{f}$. Therefore, we have

$$
\langle \overline{f}\rangle=\overline{f}\text{.}
$$

Combining above results, we have

$$
\langle f\rangle=\overline{f}\text{.}
$$

This is a key result that is given by the ergodicity assumption.

## Problems about the ergodicity assumption

During the above discussion, we are not very precise about what do we mean by $T\to\infty$. Ergodicity says that the system will visit all possible configurations at the long time limit, but how long? If the time scale for that to be achieved is $T_{Poincaré}\sim e^N$, what is the use of this mathematical hypothesis which will never be achieved in a physical system? This time scale is the [Poincaré cycle](https://en.wikipedia.org/wiki/Poincar%C3%A9_recurrence_theorem). On the other hand, the measurment to our system is usually done within a time scale that is small comparing with the time scale of observing our system, *i.e.*, $\Delta T_{measure}\ll T_{observe}\ll T_{Poincaré}$. That also suggest, thermodynamics, which is a phenomenological theory based on experimental observables, should be justified with a small portion of the accessible phase space since the time scale for measurement is only enough for the system to reaches a small portion of the accessible phase space. How come we sample our phase space evenly and use that as a support for the connection between thermodynamics and statistical mechanics? 

When we think about what ergodicity really gives us, it basically rationalize the statement that every initial condition will reach a statistical mechanics ensemble description. The stationary description, thermodynamics, will be connected with ensemble description. Are there other ways to make the connection without using the ergodicity assumption? Once we reach the ensemble description we do not need the ergodicity anyway. How to reconcile the above mentioned problems?

One possible way out is to notice two important phenomenological constraints:
* (F1) Isolated system will eventually arrive a status that the macroscopic observables are independent of time.
* (F2) The observation time scale for thermodynamic coordinates(extensive macroscopic observables) is very short.

As we have discussed, (F2) suggest our system from an arbitary initial condition($\xi_a$) will only visit its neighboring configurations, $\xi\in n(\xi_a)$, (a little corner of the accessible phase space) in our lab. (F1) suggest that if we wait long enough and perform the same measurement again, the same measurement will give us the same result. However, this time, our system will start in another corner of the accessible phase space with different initial condition ($\xi_b$), and again it will only visit its neighboring configurations, $\xi\in n(\xi_b)$, during the measurment time.

One rational conclusion we can get is: the thermodynamics provided by the two patches of phase space, $n(\xi_a)$ and $n(\xi_b)$, are identical. We never specify how big is the patch, $\xi_a$ and $\xi_b$ are also choosen in a arbitary fashion, but we know the thermodynamics is the same in general. A very bold but reasonalbe guess is: almost every configurations give the same thermodynamics. 

```{figure} /images/single_state_ensemble.pdf
---
width: 750px
name: single_state_ensemble-fig
---
Schematic picture for identical thermodynamics for every microscopic configurations.
```
To know thermodynamics, we only need to sample a single microstate. In classial mechanics, there is no nature energy unit to isolate a configuration, so we choose a window of energy $[E-\Delta E,E]$ and sample all those states in microcanonical ensemble, we then put $\Delta E\to0$ to reach the single state ensemble. In quantum system, the energy is quantized, we can really select a single state and use it to construct thermodynamics.

## Derivation of Boltzmann's postulate

The above statement seems very surpricing. Can we use this understanding to get some consistency statement? For example, to understand Boltzmann's postulate?

Suppose we have a system described by a Hamiltonian, $H(\lambda)$, with an external control parameter $\lambda$. We can express the phase space volume as

$$
\Gamma_E=\int_{E} d\Gamma =\int d\Gamma \Theta_{\Delta E}(H-E)\text{.}
$$

Here, $\Theta_{\Delta E}(H-E)=1$ if the energy of the system is in the shell $[E-\Delta E, E]$.

The microcanonical density operator is

$$
\rho=\frac{1}{\Gamma_E}\sum_{\epsilon} |
\epsilon\rangle \Theta_{\Delta E}(\epsilon-E)\langle \epsilon|\text{.}
$$ 

Here $H|\epsilon\rangle=\epsilon|\epsilon\rangle$. The density matrix normalization condition suggest

$$
Tr\left[\rho\right]=1=\frac{1}{\Gamma_E}\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\text{.}
$$

By control the parameter $\lambda$, we can do work to the system. Suppose we have internal energy change $\delta E$ as we vary the external parameter by $\delta \lambda$. The normalization condition should be maintained during this process, so we anticipate

$$
0=\delta\left[\frac{1}{\Gamma_E}\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]
$$

Here, we recall $\delta f(\vec{x})=f(\vec{x}+\delta \vec{x})-f(\vec{x})$.

$$
&\delta\left[\frac{1}{\Gamma_E}\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]\\
&= \left[\frac{1}{\Gamma_{E+\delta E}}\sum_{\epsilon} \Theta_{\Delta E}(\epsilon+\delta \epsilon-(E+\delta E))\right]
-\left[\frac{1}{\Gamma_E}\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]
$$

Now we can expand everything to leading order, we have

$$
RHS
&=\left[\frac{-\delta \Gamma_E}{\Gamma_E^2}\right]\left[\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]\\
&+\left[\frac{1}{\Gamma_E}\right]\left[\sum_{\epsilon} \frac{\partial}{\partial \epsilon}\Theta_{\Delta E}(\epsilon-E)\delta \epsilon+\sum_{\epsilon} \frac{\partial}{\partial E}\Theta_{\Delta E}(\epsilon-E)\delta E \right]+\mathcal{O}(\delta^2(\cdots))
$$

We can combine the second term which gives us

$$
\frac{\delta \Gamma_E}{\Gamma_E}=\frac{1}{\Gamma_E}\sum_{\epsilon} \frac{\partial}{\partial (-E)}\Theta_{\Delta E}(\epsilon-E)(\delta \epsilon-\delta E) 
$$

The normalization condition suggests

$$
&\partial_E\left[\frac{1}{\Gamma_E}\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]=0\\
&=\frac{1}{\Gamma_E}\partial_E\left[\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]+\left(-\Gamma_E^{-2}\right)\partial_E \Gamma_E\left[\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]\text{.}
$$

This identity gives

$$
\frac{1}{\Gamma_E}\frac{\partial}{\partial E}\left[\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]=\frac{1}{\Gamma_E^2}\frac{\partial \Gamma_E}{\partial E}\left[\sum_{\epsilon} \Theta_{\Delta E}(\epsilon-E)\right]\text{.}
$$

Most microscopic configurations give identical thermodynamics, therefore $\delta \epsilon$ and $\delta' W$(the work done by tuning $\delta \lambda$) are identical for all microscopic configurations.

The above equality gives

$$
\delta log(\Gamma_E)&=(\delta E-\delta' W)\frac{1}{\Gamma_E}\sum_{\epsilon} \left(\frac{\partial}{\partial E}\right)\left(\Theta_{\Delta E}(\epsilon-E)\right)\\
&=\delta' Q \frac{1}{\Gamma_E}\frac{\partial \Gamma_E}{\partial E}\left(\frac{1}{\Gamma_E}\sum_{\epsilon}\Theta_{\Delta E}(\epsilon-E)\right)\\
&=\delta' Q \frac{\partial log \Gamma_E}{\partial E}\left(1\right)\text{.}
$$

For ideal gas, we can explicitly calculate the quantitity $\frac{\partial \Gamma_E}{\partial E}=\frac{3N}{2E}=(k_BT)^{-1}$. Also, we know $\delta S=\delta' Q/T$. Comparing those relations, we have the Boltzmann's conjucture

$$
\delta S=k_B\delta log \Gamma_E\text{ i.e.} S=k_Blog \Gamma_E\text{.}
$$

The seemly conter intuitive statement that every microscopic configurations gives the same thermodynamics can indeed lead to the Boltzmann's conjucture. However, this is just a self-consistency check. The statement seems plausible, however the above derivation is not a mathematically solid proof for the statement.
