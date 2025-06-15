[[Dark Matter]]
[[Hubble Parameter]]
## Cosmological Principle
The universe is homogeneous and isotropic + Copernican principle "We are not in a special place".
## Friedmann-Robertson-Walker-Lemaître Metric
Referece: Sean Carroll *Spacetime and Geometry*
Use $(-+++)$ convention and geometrical unit $c=1$
In $(t,r,\theta,\phi)$ coordinates
$$
\mathrm{d}s^2 = -\mathrm{d}t^2 + a(t)\left[\frac{\mathrm{d}r^2}{1-Kr^2} + r^2\mathrm{d}\Omega^2\right]
$$
alternatively in $(t, \chi, \theta,\phi)$ comoving coordinates
$$
\mathrm{d}s^2 = -\mathrm{d}t^2 + a(t)R_0\left[\mathrm{d}\chi^2 + S_k^2(\chi)\mathrm{d}\Omega^2\right]
$$
(They are not only equivalent, but also equal.)

There are two conventions of dimensions here
1.  Dimensionless scale factor $a(t)$, curvature $K$ of dimension $[L]^{-2}$, and $r$ of dimension $[L]$. Often adopted in astronomy. In this choice $K$ can take arbitrary values.
2. Scale factor $R(t)$ of dimension $[L]$, dimensionless curvature $\kappa$, and dimensionless comoving coordinates $r$. In this choice $\kappa = {-1, 0, +1}$. And $a(t)$ is sometimes denoted as $R(t)$.

The *spatial curvature* is characterized by the Ricci scalar contracted from the spatial part of metric $g_{ij}$, which in FLRW metric is
$$
^{(3)}R = \frac{6K}{a(t)^2}
$$
In either conventiosn, $^{(3)}R$ has the dimension of $[L]^{-2}$. To see what this result means, we note that the curvature of a sphere is $^{(3)}R = 2 / r^2$. Thus for positive curvature, we say the geometry of the universe is sphere-like, and the radius of the sphere is $r = a^2(t) K / 3$, or $R^2(t) / 3$ for the $\kappa=\{1,0,-1\}$ convention. 

We also see that $\dot{a}(t)>0$ expansion drives $^{(3)}R\rightarrow 0$. 
## Friedmann Equations
$$
\frac{{\dot a}^2}{a^2} + \frac{k}{a^2} = \frac{8\pi G}{3}\rho,
$$
$$
\frac{\ddot a}{a} = -\frac{4\pi G}{3}(\rho + 3p),
$$
$$
\dot \rho + 3H(\rho + p) = 0
$$
Note: 
- Two out of the three equations are independent
- The third equation is sometimes called the continuity equation.
- For a homogeneous scalar field, the third equation gives the inflation field equation of motion $\ddot\phi+3H\dot\phi+V_{,\phi} =0$.

**Solutions to the Friedmann equations**

|           | $w$ | $\rho(a)$ | $a(t)$      | $a(\eta)$         | $\eta_i$  | $\eta(t)$   | $\eta(a)$ |
| --------- | --- | --------- | ----------- | ----------------- | --------- | ----------- | --------- |
| MD        | 0   | $a^{-3}$  | $t^{2/3}$   | $\eta^2$          | 0         | $t^{1 / 3}$ | $a^{1/2}$ |
| RD        | 1/3 | $a^{-4}$  | $t^{1 / 2}$ | $\eta$            | 0         | $t^{1 /2}$  | $a$       |
| $\Lambda$ | -1  | const.    | $e^{Ht}$    | $-\frac{1}{\eta}$ | $-\infty$ |             |           |

### Newtonian derivation
The Friedmann Equation can fomally be derived from Newtonian physics, without General Relativity. It is not a GR effect. Consider a ball with radius $a(t)$. The total mass inside the ball would be $M$. Assume that there is no matter exchange between inside and the outside of the ball, hence the mass $M=M(<a)=\text{const.}$ stays constant.

Start from Newton's second law
$$
\frac{d^2a(t)}{dt^2} = - \frac{GM}{a^2(t)}
$$

imposing a useful transformation
$$
\frac{d^2a(t)}{dt^2} = \frac{d}{dt} \frac{da}{dt} = \frac{da}{dt} \frac{d}{da} \frac{da}{dt} = \dot{a} \frac{d}{da} \dot{a} = \frac{1}{2} \frac{d}{da}(\dot{a}^2)
$$
The result can be easily integrated, denoting the integration constant as $\kappa$ on the LHS
$$
\dot{a}^2 + \kappa = 2\frac{GM}{a(t)}
$$

Expressing $M = \frac{4\pi}{3}\rho(t) a(t)^3$. Here $\rho(t)$ changes as $a(t)^{-3}$ to make $M$ constant over time. Then we have
$$
\frac{\dot{a}^2}{a^2} + \frac{\kappa}{a^2} = \frac{8\pi G}{3}\rho(t)
$$

You might want to ask, in Friedmann equations we take into account for radiation (relativistic matter which scales with $a^{-4}$) and dark energy (which is guessed to scale with some $a^{-3(w+1)}$ we are not sure of), where are those stuff here? It's because they are not thought to interact with gravity in newtonian physics. 

Also directly from Newton's second law, divide the equation by $a(t)$ gives the second Friedmann equation, but without the pressure term.
$$
\frac{\ddot{a}}{a} = -\frac{4\pi G}{3}\rho
$$
Why Einstein’s equations are needed if $p\neq 0$? – For non-relativistic matter $p ≪ ρ$, while for the relativistic matter $p = \frac{1}{3} ρ$. Meaning the pressure term is only important to describe gravitation of relativistic matter.
### Radiation dominated universe (early universe)
The Friedmann equation can be written as
$$
\frac{\dot{a}^2}{a^2} = H_0^2\Omega_{r,0} a^{-4},
$$
it follows
$$
ada = H_0\sqrt{\Omega_{r,0}} dt
$$
integration yields
$$
\frac{1}{2} a^2 = H_0\sqrt{\Omega_{r,0}} t + \text{const.}
$$
Initial condition $a=0$ when $t=0$, so the integration constant is $0$. And the result
$$
a(t) = \sqrt{2H_0\Omega_{r,0}^{1/2}} t^{1/2} = \left( \frac{32\pi G}{3}\rho_{r,0} \right)^{1/4} t^{1/2} 
$$
From here we also have some other important implications. Such as the relativistic matter density in radiation dominated universe (early universe)
$$
\rho_r(t) =  \rho_{r,0} a(t)^{-4} = \frac{3}{32\pi G} \frac{1}{t^2}
$$
Combining the relativistic matter (matter with $\langle p\rangle \gtrsim m$) density as a function of temperature (this equation is deduced by integrating the BE and FD distribution)
$$
\rho_r = \frac{\pi^2}{30}g_* T^4,\qquad g_* = \sum_\text{boson species} g_i + \frac{7}{8} \sum_\text{fermion species} g_i
$$
we can deduce temperature as a function of time or the scale factor in the early radiation dominated epoch ($k_B = \hbar = c = 1$ units)
$$
T = \left( \frac{30}{\pi^2} \frac{\rho_{r,0}}{g_*} \right)^{1/4} a^{-1} = \left( \frac{45}{32\pi^3 Gg_*} \right)^{1/4} t^{-1/2}
$$

## Cosmology parameters
We can rewrite the first Friedmann equation by
$$
\frac{H(a)^2}{H_0^2} = \frac{8\pi G}{3H_0^2}(\rho_m(a) + \rho_r(a) + \rho_\Lambda) - \frac{k}{H_0^2a^2}
$$

**Matter combination** decides everything: the curvature of the universe, the acceleration/deceleration of the universe.
$$\Omega_m := \frac{\rho_m}{\rho_c}=\frac{8\pi G}{3H^2}\rho_m,\quad \Omega_\Lambda := \frac{8\pi G}{3 H^2}\rho_\Lambda, \quad\Omega_r:= \frac{8\pi G}{3H^2}\rho_r, \quad\Omega_k := -\frac{k}{a^2H^2}$$
and the Friedmann equation can be written as $$\Omega_m + \Omega_\Lambda + \Omega_r + \Omega_k = 1$$
This sum equals one hold true at any cosmic time because of the Friedman equation and some clever definition of $\Omega_k$, which is not actually the density of anything!
$$\Omega_{tot} := \Omega_m + \Omega_\Lambda + \Omega_r = 1 + \frac{k}{a^2H^2}$$
Or in more useful form, multiply by $\frac{H^2}{H_0^2}$
$$
\boxed{\frac{H^2}{H_0^2} = \frac{\Omega_{m,0}}{a^3} + \frac{\Omega_{r,0}}{a^4} + \frac{\Omega_{k,0}}{a^2} + \Omega_\Lambda}
$$
where
$$
\Omega_{m,0} := \frac{8\pi G}{3 H_0^2}\rho_{m,0}, \quad\Omega_{r,0}:= \frac{8\pi G}{3H_0^2}\rho_{r,0}, \quad\Omega_{k,0} := -\frac{k}{H_0^2}
$$
And $\Omega_i$ relates to $\Omega_{i,0}$ by 
$$
\Omega_m = \Omega_{m,0}a^{-3} \frac{H_0^2}{H^2},\quad \Omega_r = \Omega_{r,0}a^{-4} \frac{H_0^2}{H^2}, \quad \Omega_k = \Omega_{k,0} a^{-2} \frac{H_0^2}{H^2}
$$
which means the curvature of the universe is decided by the total density of matter. Note that $\Omega_{tot}$ is not a constant over time.
Where $\Omega_i:=\dfrac{\rho_i}{\rho_c}, \rho_c := \dfrac{3H^2}{8\pi G}, H := \dfrac{\dot a}{a}$.

Now $H_0 = h\times100\,\mathrm{km/s/Mpc},\quad h\sim O(1)$. Then the critical density today is 
$\rho_c := \dfrac{3H_0^2}{8\pi G} = 1.879 h^2\times 10^{-29}\mathrm{g\,cm^{-3}}$

### Deceleration parameter
$$q:=-\dfrac{\ddot{a}a}{\dot{a}^2}=\frac{1}{2}\Omega_m + \Omega_r - \Omega_\Lambda$$
or equivalently
$$
q \frac{H^2}{H_0^2} = \frac{1}{2} \frac{\Omega_{m,0}}{a^3} + \frac{\Omega_{r,0}}{a^4} - \Omega_{\Lambda,0}
$$

