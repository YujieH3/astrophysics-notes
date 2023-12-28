## Maxwell's equations
(from Introduction to Classical Field Theory by Charles G. Torre)
The force on a test particle with electric charge $q$ at spacetime event $(\vec r, t)$ is given by
$$
\vec{F}(\vec r, t) = q\vec E(\vec r, t) + \frac{q}{c}(\vec v(t) \times \vec{B}(\vec{r},t))
$$
And the electromagnetic field is determined from the charge distribution that is present via the Maxwell equations
$$
\begin{align}
\nabla \times \vec B - \frac{1}{c}\frac{\partial \vec E}{\partial t} &= \frac{4\pi}{c}\vec j,\\
\nabla \cdot \vec E &= 4\pi\rho,\\
\nabla \times \vec E + \frac{1}{c}\frac{\partial \vec B}{\partial t} &= 0,\\
\nabla \cdot \vec B &= 0.
\end{align}
$$
In geometric units
$$
\begin{align}
\nabla \times \vec B - \partial_t \vec E &= \vec J,\\
\nabla \cdot \vec E &= \rho,\\
\nabla \times \vec E + \partial_t \vec B &= 0,\\
\nabla \cdot \vec B &= 0.
\end{align}
$$
And in index notation with $J_\mu = (\rho, \vec J)$
$$
\begin{align}
\tilde \epsilon^{ijk}\partial_jB_k - \partial_0 E^i &= J^i,\\
\partial_i E^i &= J^0,\\
\tilde \epsilon^{ijk}\partial_jE_k + \partial_0 B^i &= 0,\\
\partial_iB^i &= 0.
\end{align}
$$
Define electromagnetic tensor
$$
\begin{align}
F^{0i} &= E^i,\\
F^{ij} &= \tilde\epsilon^{ijk}B_k.
\end{align}
$$
Then the Maxwell equations becomes
$$
\begin{align}
\partial_\mu F^{\nu\mu} &= J^\nu\\
\partial_{[\mu}F_{\nu\lambda]} &= 0
\end{align}
$$
## Electromagnetism Field Theory

Define scalar potential and vector potential, a scalar field $\phi$ and a vector field $\vec A$ by
$$\vec E = -\nabla \phi - \frac{\partial \vec A}{\partial t},\quad \vec B = \nabla \times \vec A$$
By this definition $\vec E,\vec B$ automatically satisfy second and fourth of the Maxwell equations. Define 4-potential $A_\mu = (-\phi, A_i), i=1,2,3$. Then electromagnetic tensor is
$$F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu$$

The Lagrangian is given by
$$\mathcal{L} = - \frac{1}{4}F_{\mu\nu}F^{\mu\nu} - J^\mu A_{\mu}$$
and the action
$$
S = \int  \left[- \frac{1}{4}F_{\mu\nu}F^{\mu\nu} - J^\mu A_{\mu}\right]\sqrt{-g} \,\mathrm d^4x
$$
The Euler-Lagrange equations
$$
- \partial_\mu F^{\mu\nu} + J^\nu = 0
$$