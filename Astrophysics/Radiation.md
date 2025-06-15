## Concepts and Terminology of Radiation

**Radiation intensity** $I_\nu$, energy emitted per unit time per unit area per frequency/wavelength per solid angle. Let dEν be the energy in radiation at frequency ν, in frequency interval dν, from solid angle dΩ, flowing through an area dA, in a time interval dt :
$$
dE_\nu = I_\nu d\nu d\Omega d\sigma \cos{\theta} dt = I_\nu d\nu d\Omega dA dt
$$
$$
I_\nu = I_\nu(\nu, \hat{n}, \vec{r}, t)
$$
- units: erg s-1 cm-2 sr-1 Hz-1. 
- sr: steradian, $4\pi$ for full sky

An alternative, equivalent (and often simpler) way to express specific intensity is by the photon occupation number $n_\gamma$
$$
n_\gamma = \frac{c^2}{2h\nu^3} I_\nu
$$

(Rayleigh-Jeans) brightness temperature, equals to thermal temperature in radio regime $kT\gg h\nu$
$$T_b(\nu) = \frac{c^2}{2k\nu^2} I_\nu$$

**Radiation flux** $\pi F_\nu$
$$
	\pi F_\nu = \int_{2\pi} I_\nu(\theta) \cos{\theta} d\omega =
	\int_0^{2\pi} d\phi \int_0^{\pi/2} \sin\theta d\theta  \, I_\nu \cos\theta,
$$
Note that the integration span only half the steradians ($2\pi$) in the direction of emission.

- 辐射流矢量 $\pi \vec F_\nu$
- 平均辐射强度 $J_\nu$
$$
	J_\nu = \dfrac{1}{4\pi} \int_{4\pi}I_\nu(\theta)d\omega,
$$
- Energy density $U_\nu$ (erg cm-3 Hz-1)
$$
	U_\nu = \dfrac{1}{c} \int_{4\pi} I_\nu d\omega,
$$
- 辐射压力 $P_{R,\nu}$
$$
	P_{R,\nu} = \frac{1}{c}\int_{4\pi}I_\nu(\theta)\cos^2\theta d\omega,
$$
- 辐射压力张量 $\vec P_{R,\nu}$

## Other Concepts
### Surface brightness 
The surface brightness of a galaxy $I(x)$ is the amount of light on the sky at a particular point $x$ on the image. Consider a small patch of side $d$ in a galaxy located at a angular diameter distance $D_A$ and luminosity distance $D_L$. It will subtend an angle $\theta = d/D_A$ on the sky. If the combined luminosity of all the stars in this region is $L$, its apparent brightness is $F = L/(4πD_L^2)$.
Therefore the surface brightness
$$I(x) = F/α^2 = \frac{L}{4\pi D_L^2}\frac{D_A^2}{d^2} = \frac{L}{4\pi d^2}\frac{1}{(1+z)^4}.$$
Note the last equation holds only under a flat geometry! (See [[Cosmological Distances]]) The appropriate units of $I(x)$ are $L_\odot/\mathrm{pc}^2$.

## Radiative Transfer Equations

- Optical depth $\tau_\nu$
$$
\tau_\nu = \int_0^s \chi_\nu\rho ds,\quad d\tau_\nu = \chi_\nu \rho ds,
$$
$\tau_\nu \gg 1$: optically thick; $\tau_\nu \ll 1$: optically thin
- Emission coefficient $j_\nu$
$$
dE_\nu = j_\nu dm ds dt d\nu d\omega
$$
- Absorption coefficient $\chi_\nu$
$$
dE_\nu = -\chi_\nu I_\nu dm dt d\nu d\omega
$$
The radiative transfer equation is simply energy conservation:
$$
\boxed{\frac{dI_\nu}{ds} = -\chi_\nu I_\nu \rho + j_\nu\rho}
$$

## References
1. 《恒星大气物理》汪珍如 曲钦岳
2. Rijksuniversiteit Groningen galaxy course: https://www.astro.rug.nl/~ahelmi/galaxies_course/class_VII-E/ellip-06.pdf
3. Lecture notes of Paul van der Werf, *Interstellar Medium*
