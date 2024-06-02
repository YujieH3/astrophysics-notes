[[Dark Matter]]
[[Hubble Parameter]]
### Cosmological Principle
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
## Friedmann Equations
The first Friedmann Equation
$$\boxed{\frac{{\dot a}^2}{a^2} + \frac{k}{a^2} = \frac{8\pi G}{3}\sum_i\rho_i}$$
The curvature term $\frac{k}{a^2}$ is the integration constant if you integrate from Newtonian approach, $k$ as a "minus total energy of the system". *Turns out the relativistic correction is unimportant, the equation deduced from GR and Newtonian gravity is the same*.

The second Friedmann Equation
$$\boxed{\frac{\ddot a}{a} = -\frac{4\pi G}{3}\sum_i(\rho_i + 3p_i)}$$
Combining the above we have the third Friedmann Equation
$$\boxed{\dot \rho + \frac{3\dot a}{a}(\rho + p) = 0}$$
###### pf. Newtonian derivation
The Friedmann Equation can fomally be derived from Newtonian physics, without General Relativity. It is not a GR effect. Consider a ball with radius $r$ and 



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
## Inflation
Alan H. Guth: Inflaitionary Universe: A possible solution to the horizon and flatness problem
Flatness + horizons $\leftarrow$ inflation $\leftarrow$ GW observation (not yet)

## Nucleosynthesis
Boltzmann constant $k = 8.62\times 10^{-5} \mathrm{eV/K}$
Nucleosynthesis: proton and neutron (Baryon matter)
matter >> antimatter
Baryon number density $n_B$ . Baryon to photon ratio $\eta = n_B/n_\gamma$

