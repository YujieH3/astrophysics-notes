[[Gravitational Wave]]

What we know is that objects tends to move towards each other. A larger "amount" of matter bears a larger tendency in this sense. And a theory of gravitation is a theory that allow us to calculate how they move under this tendency.

## Newtonian Gravity
Newton's theory of gravity. In the language of force
$$
\boldsymbol F = G\frac{Mm}{r^2}\boldsymbol e(r)
$$
and then
$$\boldsymbol F = m \boldsymbol a$$
In the language of gravitational potential $\Phi$
$$\Delta^2 \Phi = 4\pi G \rho$$
and the acceleration is given by the gradient of the potential
$$\boldsymbol{a} = \Delta\Phi$$
#### Gravitational Potential Energy
Gravitational potential is define as the work produced by gravitation to move the mass points away from each other to infinitely far away, where the zero point is set, i.e. $U(r=\infty) = 0$. 
$$
U = \int_r^\infty -G\frac{m_1m_2}{r^2}dr = -G\frac{m_1m_2}{r}.
$$

#### Self Graviational Potential Energy
For a sphere of radius $R$ and total mass $M$ with constant density, the self gravitational potential energy is
$$
U = -\frac{3}{5}G\frac{M^2}{R}.
$$
Proof
$$
\begin{align}
U &= \int_0^{M}-G\frac{M(r)}{r}dm\\
&= \int_0^R-G\frac{Mr^3/R^3}{r}\rho4\pi r^2dr,\quad \rho=\frac{M}{4/3\pi R^3}\\
&= -G\frac{3M^2}{R^6}\int_0^Rr^4dr\\
&= -\frac{3}{5}G\frac{M^2}{R}.
\end{align}
$$

## General relativity
Einstein's theory of gravity. Spacetime curves according to the Einstein's equation
$$R_{\mu\nu} - \frac{1}{2}Rg_{\mu\nu} = 8\pi GT_{\mu\nu}$$
Objects move according to the geodesic equation
$$\frac{d^2x^\mu}{d\lambda^2} + \Gamma^\mu_{\rho\sigma}\frac{dx^\rho}{d\lambda}\frac{dx^\sigma}{d\lambda} = 0$$
#### Schwarzschild metric
$$
ds^2 = -\left(1-\frac{2GM}{r}\right)dt^2 + \frac{dr^2}{(1-\frac{2GM}{r})} +r^2(d\theta^2 + \sin^2\theta d\phi^2 )
$$
