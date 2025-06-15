# Statistical Distributions: Maxwell-Boltzmann, Fermi-Dirac, and Bose-Einstein
Expectation value (average) of parameter $X$ following distribution $f$ is given by,
$$
\langle X\rangle = \int f(\boldsymbol{k}) X(\boldsymbol{k})\frac{d^3\boldsymbol{k}}{(2\pi)^3},
$$
where $k$ is the momentum. 

The Boltzmann constant $k_B$ is set to 1. Also $c=1$.

## Maxwell-Boltzmann Distribution
$$
f_{MB} = e^{-(\epsilon(p) - \mu)/T}
$$

## Fermi-Dirac Distribution
$$
f_{FD} = \frac{1}{e^{(\epsilon(p) - \mu)/T} + 1}
$$

## Bose-Einstein Distribution
$$
f_{BE} = \frac{1}{e^{(\epsilon(p) - \mu)/T} - 1}
$$
### Number density of Photons
$$
n_\gamma (T) = g_\gamma \int \frac{d^3 \boldsymbol{k}}{(2\pi)^3} \frac{1}{e^{|k|/T} - 1} = \frac{2\zeta(3)}{\pi^2} T^3 \approx \frac{2.4}{\pi^2} T^3
$$
### Derivation of Stefan-Boltzmann Law
$$
\rho_\gamma = g_\gamma \int \frac{d^3 \boldsymbol{k}}{(2\pi)^3} \frac{E(\boldsymbol{k})}{e^{|k|/T} - 1} = \frac{\pi^2}{15} T^4 = \frac{4}{c} \sigma_{SB} T^4
$$
Where we restored the units from $k_B = \hbar = c = 1$. $$\sigma_{SB} = \dfrac{\pi^2k_B^4}{60\hbar^3 c^2}$$