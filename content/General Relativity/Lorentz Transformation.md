[[Four Vectors]]
# Lorentz Transformation
Lorentz transformation is transformations that keep spacetime interval invariant, which is equivalent to, in matrix notation
$$
\eta = \Lambda^\top \eta \Lambda
$$
or in index notation
$$
\eta_{\rho\sigma} = \Lambda^{\mu'}\,_\rho \Lambda^{\nu'}\,_\sigma\eta_{\mu'\nu'}
$$
A rotation free Lorentz transformation is called a Lorentz boost.

In the most well-known form,
$$
\begin{align}
t' &= \gamma(t - vx)\\
x' &= \gamma(x - vx)
\end{align}
$$
where $\gamma = (1-v^2)^{-1/2}$. For vector $V$
$$
V^{\mu'} = \Lambda^{\mu'}\,_\nu V^{\nu}
$$
It's important to keep in mind that vector $V$ itself is invariant under Lorentz transformation/boost. It's merely the basis that is changing. Or explicitly
$$
\vec e_{(\mu')} = \Lambda^{\nu}\,_{\mu'}\vec e_{\nu}
$$
Where $\Lambda^{\nu}\,_{\mu'}$ is the inverse of $\Lambda^{\mu'}\,_{\nu}$.

The Lorentz boost from coordinate system $S$ to $S'$ where $S'$ is moving at velocity $v$ along the $x$-axis of $S$ is
$$
\Lambda^{\mu'}\,_\nu = 
\begin{pmatrix}
\gamma & -\gamma v & 0 & 0\\
-\gamma v & \gamma & 0 & 0\\
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{pmatrix}
$$
## Lorentz group
(From Srednicki, 2)
The set of all Lorentz transformations forms a group:
- Associative: product of any two Lorentz transformations is also a Lorentz transformation.
- Identity: There exists an identity transformation that is a Lorentz transformation, $\delta^\mu\,_\nu$
- Every Lorentz transformation has an inverse

Lorentz group has two important subgroups: 
- *proper*: $\det\Lambda = +1$; *improper*: $\det\Lambda = -1$.
- *orthochronous*: $\Lambda^0\,_0 \geq +1$. ($\Lambda^0\,_0$ can only be $\geq +1$ or $\leq -1$).

We can write infinitesimal Lorentz Transformation as
$$
\Lambda^\mu\,_\nu = \delta^\mu\,_\nu+\delta\omega^\mu\,_\nu,\quad \delta\omega_{\mu\nu} = -\delta\omega_{\nu\mu} \,(\text{d.o.f.=6})
$$
the 6 degree of freedom can be completely decomposed to three rotations with infinitesimal angle ($\delta\theta$) and three boosts with infinitesimal *rapidity* ($\delta\eta$),
$$
\delta \omega_{ij} = -\varepsilon_{ijk}\hat{n}_k\delta\theta,\quad \delta \omega_{i0} = \hat{n}_i\delta\eta
$$
Only *proper* and *orthochronous* transformations can be reached by compounding infinitesimal transformations. When a theory is said to be Lorentz invariant, this means under the proper orthochronous subgroup only.

**Parity transformation**, orthochronous but improper
$$
\mathcal{P}^\mu\,_\nu = \begin{pmatrix}
1 &  &  & \\
 & -1 &  & \\
 &  & -1 & \\
 &  &  & -1
\end{pmatrix}
$$
and **time-reversal transformation**, nonorthochronous and improper
$$
\mathcal{T}^\mu\,_\nu = \begin{pmatrix}
-1 &  &  & \\
 & 1 &  & \\
 &  & 1 & \\
 &  &  & 1
\end{pmatrix}
$$
are usually discussed separately.

