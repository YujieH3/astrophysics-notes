Johns Hopkins Turbulence Database (JHTDB): http://turbulence.pha.jhu.edu/

> [!A G Kritsuk, 2017, The structure and statistics of interstellar turbulence]
> Turbulence is ubiquitous in the interstellar medium (ISM) [1]. It organizes the ISM structure to optimize and direct energy fluxes across an enormous range of length scales within the Milky Way disk. Interstellar turbulence, however, differs from the familiar Kolmogorov homogeneous and isotropic incompressible case [2, 3] in several important respects: it is neither isotropic nor homogeneous [4]; the interstellar gas is highly compressible and magnetized; and its thermal energy is not strictly conserved. Instead, the ISM-specific radiative cooling and volumetric heating functions determine an equilibrium multiphase nature of the neutral ISM [5, 6, 7]. Nonlinear advection couples with nonlinear radiative cooling, further complicating the treatment of the ISM. We hence deal with a classical example of a hierarchical nonequilibrium dissipative system, receiving energy primarily at large scales (∼ 100 pc) from stellar feedback, extragalactic gas accretion, large-scale shear, and gravitational instabilities within the disk and loosing energy through small-scale dissipation (10−4 pc) and local radiative cooling [8].


## Kolmogorov Scaling
Kolmogorov's theory in homogeneous and isotropic incompressible turbulence. Interstellar turbulence, however, differs with this scenario in several important respects: it is neither isotropic nor homogeneous; the interstellar gas is highly compressible and magnetized; and its thermal energy is not strictly conserved.

Big whorls have little whorls,
which feed on their velocity;
And little whorls have lesser whorls,
And so on to viscosity

from: https://physics.stackexchange.com/questions/13161/physical-explanation-for-kolmogorov-5-3-spectrum-in-fluid-mechanics

The standard explanation is that there is a constant flux of energy from large eddies to smaller eddies. The time scale $\tau$ for an eddy of scale $r$ to turn over is $$\tau \sim \frac{r}{v(r)} \sim \frac{1}{kv}$$the energy density for scale $r$ is $\sim v(r)^2$, so you get an **energy flux rate** $$\epsilon \sim \frac{v^2}{\tau} \sim v^3k$$ which is assumed constant. You then estimate the **spectral energy density** as $$E \sim \frac{v^2}{k} \sim \epsilon^{2/3} k^{-2/3-1} = \epsilon^{2/3}k^{-5/3}$$
I hope that is a little better than pure dimensional analysis.

![[Kolmogorov-scaling-in-the-inertial-range.jpg]]

Driving scale