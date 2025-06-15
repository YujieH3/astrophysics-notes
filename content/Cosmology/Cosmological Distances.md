# Cosmological Distances

#### Coordinate distance, the one in the metric
as in FLRW metric (see [[Friedmann Equations#Friedmann-Robertson-Walker-Lemaître Metric]])
#### 1. Comoving distance
$$
D_C \equiv S_k(r) \equiv \int_0^r \frac{dr'}{\sqrt{1 - Kr'^2}} = \left\{
\begin{aligned}
&\arcsin(\sqrt{K}r) / \sqrt{K}, &K > 0 \\
&0, &K=0\\
&\mathrm{arcsinh} (\sqrt{-K}r) / \sqrt{-K}, &K<0\\
\end{aligned}
\right.
$$
The integration can be translate to for radial distances
$$
D_C = S_k(r) = \int \frac{dr'}{\sqrt{1-Kr'^2}} = \pm\int \frac{cdt}{a} = \pm\int \frac{cda}{\dot{a}a} = \mp \int \frac{cdz'}{H(z')}
$$
Watch out the square root sign. Choose the sign based on your problem, e.g. a light ray from $r=0$ or to $r=0$.
#### 2. Proper distance (physical distance)
$$
D_P \equiv a_o S_k(r) \rightarrow^{a_o=1} D_C
$$

#### 3. Luminosity distance
$$
D_L \equiv \frac{a_o^2}{a_e}r_e \rightarrow^{a_o=1} (1+z)^2D_A \rightarrow^{K=0}_{a_0=1} (1+z) D_C
$$
#### 4. Angular diameter distance
$$
D_A \equiv a_er_e \rightarrow^{K=0} \frac{D_C}{1+z}
$$
#### 5. Proper motion distance
$$
D_M \equiv a_0r\rightarrow ^{K=0} D_C
$$
