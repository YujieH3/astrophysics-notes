# Cluster Cosmology
[Nice lecture slides for cluster cosmology](https://www.star.bris.ac.uk/bjm/lectures/cluster-cosmology/)

#### Cluster Properties

**X-ray Luminosity** (from images or spectra) depends strongly on $\rho$, more weakly on $T$. Bremsstrahlung emission from hot ionized gas.

Emissivity of a bremsstrahlung-emitting plasma is
$$
\epsilon_\nu \propto \frac{Z^2n_en_i}{T^{1/2}}e^{-h\nu/kT}
$$
$\epsilon_\nu$ is energy emitted per unit frequency, time and volume. $n_e, n_i$ are number densities of electrons and ions. $Z$ is charge on ion. Then
$$
L_X \propto \int \epsilon_\nu d\nu dV \propto \int n_en_i T^{1/2}dV \sim \rho^2
$$

**X-ray Temperature** $kT$ (from spectra) - Fitting to observed X-ray spectra give temperature of the intra-cluster medium (ICM). $kT$ in range $\sim 1$ to $\sim 15$ keV. Gas are heated to these temperatures during cluster formation. $kT \sim \langle T \rangle$ (kinetic energy) -virial theorem-> cluster mass.

**Metal abundances in ICM** (from spectra)

**Density of ICM** (from surface brightness profile)

**Overdensity Radii** $R_\Delta$ - A radius within which the mean density is $\Delta$ times the critical density ($\rho_c$) at the cluster's redshift. Denoted as $R_\Delta$. And the total mass within $R_\Delta$ is denoted as $M_\Delta = \Delta\rho_c \dfrac{4\pi}{3}R_\Delta^3$. $\displaystyle \Delta=\frac{\rho}{\rho_c}$ and recall from [[Friedmann Equations]], $\rho_c := \dfrac{3H(z)^2}{8\pi G}$. 

Simulations show $R_{200} \sim$ virial radius: radius separating relaxed part of cluster from infalling material. $R_{500} \, (\sim 0.5 R_{200})$ is radius measured out to in typical X-ray observations. 

If a galaxy cluster is **dynamically relaxed** (no recent mergers) we expect the gas and galaxies to be virialized ([[Virial Theorem]]). 


#### Scaling Relations
Self-similar model assumes: 
- Clusters form in single collapse at $z_{obs}$
- Gravity only source of energy
Self-similar model predicts:  
- Clusters of different masses are scaled versions 
- Clusters at different $z$ identical if scaled for $\rho_c(z)$ (*This is where $E(z)$ comes in*)

![[Pasted image 20240119102924.png]]
From Kostas' DMDE lecture

Two key point of the scaling relation is the [[Virial Theorem]] and X-ray emissivity and luminosity's dependence on total mass.
$$M_\Delta = \Delta \rho_c(z) R_\Delta^3 = \Delta \rho_{c,0}E(z)^2R_\Delta^3\propto E(z)^2 R^3$$
where $E(z) = \sqrt{\Omega_m(1+z)^3 + \Omega_\Lambda}$. Recall from [[Virial Theorem]] we know that $\displaystyle T \propto \frac{M}{R}$, therefore $\boxed{M \propto E(z)^{-1} T^{3/2}}$

**X-ray emissivity & luminosity**
Emissivity $\epsilon \propto T^{1 /2} \rho_{\text{gas}}^2$ and luminosity $L_X \propto \epsilon V \propto \epsilon R^3$. Therefore
$$
L_X \propto \rho_\text{gas}^2T^{1 /2} R^3 \propto \frac{M^2}{R^6} T^{1 /2} R^3 \propto \frac{M^2}{R^3} T^{1 /2} \propto \frac{T^3}{M}T^{1 /2} \propto E(z)T^{2}
$$
So $\boxed{L_X \propto E(z)T^2}$

Also (*derivation needed?*)
$$
\boxed{Y_{SZ} \propto E(z)^{-1}T^{2.5}}
$$
From $M-T$, $L_X-T$, $Y_{SZ}-T$ relations we can readily obtain $L_X-Y_{SZ}$, $L_X-M$, $Y_{SZ}-M$,
$$
\begin{align}
L_X & \propto E(z)^{9/5} Y_{SZ}^{4/5} \\
L_X & \propto E(z)^{7/3}M^{4/3} \\
\end{align}
$$
$$
\boxed{Y_{SZ} \propto E(z)^{2/3} M^{5/3}}
$$

#### Soft X-ray 0.1-2.4 keV
for soft x-ray we expect $L_X \sim E(z) T^{3/2}$ instead of 2. Other $L_X$ related relations also differs as listed. 
$$
\boxed{
\begin{align}
L_X & \propto E(z)^{8/5} Y_{SZ}^{3/5} \\
L_X & \propto E(z)^{2} M^{1} \\
\end{align}
}
$$


## Cosmology implication
$$
M_\text{gas} \sim d_A^{5/2}
$$
For $L_X-T$ and $Y_{SZ}-T$ relations
$$
\frac{H_0}{H_{0,\text{all}}} = \left( \frac{A}{A_{\text{all}}} \right)^{1/2}
$$
For $M_{gas}-T$
$$
\frac{H_0}{H_{0,\text{all}}} = \left( \frac{A}{A_{\text{all}}} \right)^{2/5}
$$
