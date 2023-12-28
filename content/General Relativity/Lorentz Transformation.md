[[Four Vectors]]
## Lorentz Transformation
Lorentz transformation is transformations that keep spacetime interval invariant, which is equivalent to, in matrix notation
$$\eta = \Lambda^\top \eta \Lambda$$
or in index notation
$$\eta_{\rho\sigma} = \Lambda^{\mu'}\,_\rho \Lambda^{\nu'}\,_\sigma\eta_{\mu'\nu'}$$
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
