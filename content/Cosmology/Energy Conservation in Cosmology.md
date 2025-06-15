# Energy Conservation in Cosmology

A vector field $\xi^\mu$ is a **Killing vector** if it preserves the metric under its flow:

$$
\mathcal{L}_\xi g_{\mu\nu} = \nabla_\mu \xi_\nu + \nabla_\nu \xi_\mu = 0
$$

In FLRW metric, the only nontrivial Christoffels are:

$$
\Gamma^0_{ij} = a \dot{a} \delta_{ij}, \quad \Gamma^i_{0j} = \frac{\dot{a}}{a} \delta^i_j
$$

The Lie derivative is
$$
(\nabla_0 \xi_0 + \nabla_0 \xi_0) = 0, \quad
(\nabla_0 \xi_i + \nabla_i \xi_0) = 0, \quad
(\nabla_i \xi_j + \nabla_j \xi_i) = 2 \Gamma^0_{ij} \xi_0 = 2 a \dot{a} \delta_{ij} \neq 0
$$

Thus, the time vector $\xi^\mu = \partial_t$ is not a Killing vector unless $\dot{a} = 0$, i.e., unless the scale factor is constant (i.e., static spacetime). This is approximately true in the Minkowski limit, infinitely far back in time, $\eta \rightarrow -\infty$.

If a particle moves in a spacetime with a timelike Killing vector $\xi^\mu$, then the quantity:

$$
E = - \xi^\mu p_\mu
$$

is conserved along the geodesic (where $p^\mu = m u^\mu$).

But if no such $\xi^\mu$ exists (e.g., in FRW), then this "energy" is **not conserved** — e.g., photons redshift:
$$
E \propto \frac{1}{a(t)}
$$

Even more generally, in GR, the local conservation law:

$$
\nabla_\mu T^{\mu\nu} = 0
$$

does not imply global conservation of energy unless spacetime symmetries (Killing vectors) exist.
