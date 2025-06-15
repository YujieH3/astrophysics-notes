Wenzel-Kramers-Brillouin + Jeffreys. Also a semiclassical approximation! Resembles [[Bohr-Sommerfeld quantization]].
probability amplitude $\psi$ that a particle from $\vec{r_i}$ reaches $\vec{r_f}$ is the sum of the amplitudes along all *classical* paths connecting $\vec{r_i}$ to $\vec{r_f}$
$$
\psi = \sum_\text{paths}\frac{1}{\sqrt{\nu(\vec r_f)}} \exp\left(\frac{i}{\hbar} \int_\vec{r_i}^\vec{r_f} \vec{p}\cdot d\vec l + i\gamma \right)
$$
- factor $1/\sqrt{\nu}$ is to keep current density $j=\nu|\psi|^2$ constant along path
- phase shift $\gamma$ (Maslov index) is $\pi$ at hard wall, where $\psi=0$, so that incident and reflected waves cancel. At a smooth turning point, $\nu$ changes sign, $\gamma=-\pi/2$.