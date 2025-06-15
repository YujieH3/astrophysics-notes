The Heisenberg equation of motion is
$$
i\hbar \frac{d}{dt} \hat{O} = [\hat{O}, \hat{H}]
$$
which assumes time dependence in operators rather than states, as opposed to the [[Schrödinger picture]]. The Heisenberg picture is very useful along with [[Path integral formulation]] in quantum field theory.

Some implications:
1. The time evolution of a operator is therefore, 
$$
\hat{O}(t) = e^{i\hat{H}t}\hat{O}(0) e^{-i\hat{H}t}
$$
We take $\hbar =1$. You can see this by substituting into the above Heisenberg equation of motion. If generalised to four vectors
$$
\hat{O}(t,x) = e^{i\hat{P}_\mu x^\mu}\hat{O}(0) e^{-i\hat{P}_\mu x^\mu}
$$
where $P^\mu = (H,p^i)$.

2. The Heisenberg equation implies that operator commuting with the Hamiltonian implies conservation, as in the quantity is invariant in evolution. If $[O, H]=0$, then
$$\frac{dO}{dt} = 0.$$
3. We can define instantaneous eigenstates as
$$
\hat O(t)|o,t\rangle=o|o,t\rangle, \quad \text{where }|o,t\rangle = e^{i\hat Ht}|o\rangle
$$
such that
$$
\hat O(t)|o,t\rangle=o|o,t\rangle\rightarrow e^{i\hat H t}\hat{O}\cancel{e^{-i\hat Ht} e^{i\hat Ht}}|o\rangle= e^{i\hat H t}o|o\rangle \implies \hat O|o\rangle = o|o\rangle
$$
Note the sign difference between here $|o,t\rangle = e^{i\hat Ht}|o\rangle$ and the [[Schrödinger picture]] where $|o,t\rangle = e^{i\hat Ht}|o\rangle$.