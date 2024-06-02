# Radiation
## Concepts and Terminology of Radiation

- Radiation intensity (辐射强度) $I_\nu$, energy emitted per unit time per unit area per frequency/wavelength per solid angle
$$
	dE_\nu = I_\nu d\sigma \cos{\theta} d\nu dt d\omega,
$$
- Radiation flux (辐射流) $\pi F_\nu$
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
- 辐射密度 $U_\nu$
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
$\tau_\nu \gg 1$ 称光学厚
$\tau_\nu \ll 1$ 称光学薄
- 发射系数 $j_\nu$
$$
dE_\nu = j_\nu dm ds dt d\nu d\omega
$$
- 吸收系数 $\chi_\nu$
$$
dE_\nu = -\chi_\nu I_\nu dm dt d\nu d\omega
$$

则根据能量守恒可推导出辐射转移方程为
$$
\boxed{\frac{dI_\nu}{ds} = -\chi_\nu I_\nu \rho + j_\nu\rho}
$$
其中$ds$沿着光线传播的方向

## Reference
1. 《恒星大气物理》汪珍如 曲钦岳
2. Rijksuniversiteit Groningen galaxy course: https://www.astro.rug.nl/~ahelmi/galaxies_course/class_VII-E/ellip-06.pdf

