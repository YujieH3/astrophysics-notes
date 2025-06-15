A equivalent formulation of quantum mechanics is the path integral formulation (the others are the [[Schrödinger picture]] and [[Heisenberg picture]]). The path integral formulation is considerably more convoluted, however it provides valuable insights to extensions to quantum field theories. 

In the path integral formulation, the amplitude goes to
$$
P = \int \mathcal{D}p\,\mathcal{D}q \,e^{i\frac{S}{\hbar}}
$$
Specifically, the probability that a particle at $q'$ position at time $t'$ to move to $q''$ at $t''$ is
$$
\langle q'',t''|q',t'\rangle = \int\mathcal{D}q \mathcal{D}p\exp\left[\frac{i}{\hbar}\int_{t'}^{t''}dt (p\dot{q} - H)\right]
$$


Note:
1. What are $\mathcal{D}p$ and $\mathcal{D}q$?
$$
\begin{align}
\mathcal{D}q = \lim_{N\rightarrow \infty} \prod_{k=0}^{N-1} dq_k ,\\
\mathcal{D}p = \lim_{N\rightarrow \infty}\prod_{j=0}^N \frac{dp_j}{(2\pi)^N},
\end{align}
$$
where $q_1, q_2, ..., q_N$ are each subsequent in time, $q(t_1), q(t_2), ..., q(t_N)$, with $t_1 < \cdots <t_N$. Same for $p$. There is a freedom of a normalisation constant. 
2. The path integral is a limit.
3. If $H$ is no more than quadratic in the momenta (as is the case for $H=\frac{P^2}{2m}+V(Q)$), then we can integrate over $p$, then
$$
\langle q'',t''|q',t'\rangle = \int\mathcal{D}q \exp\left[\frac{i}{\hbar}\int_{t'}^{t''}dt \,L(q(t),\dot{q}(t))\right]
$$
discretising over time steps of $dt = \epsilon$ and integrating over $p$ gives a integration constant, which we absorb into the definition of $\mathcal{D}q$
$$
\mathcal{D}q = \lim_{N\rightarrow \infty} \left(\frac{m\hbar}{2\pi i\epsilon}\right)^{\frac{N}{2}} \prod_{k=0}^{N-1} dq_k
$$

Now that given a hamiltonian/lagrangian, we should be in principle able to calculate the transition rate/probability between some initial $q'(t')$ and final $q''(t'')$ state. 

## Interaction
Taking $\hbar=1$ from here on. Adding interaction terms in your action
$$

$$
