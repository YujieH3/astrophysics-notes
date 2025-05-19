# Basic terminologies
### Expectation / Mean / Variance
**Expectation $E$** or **Mean $\mu$**. For discrete distribution $p_i$, 
$$
\mu = \sum^n_{i=1}p_ix_i
$$
 For continuous distribution $f(x)$,
$$
\mu = \int xf(x)dx
$$
In general the expectation value of $\cdot$ is,
$$
E(\cdot) = \langle \cdot \rangle = \int \cdot f(x) dx
$$
Properties:
- Linearity: $\langle ax + bx^2\rangle = a\langle x\rangle + b\langle x^2\rangle$
- *When in doubt, go back to integral.*

**Variance $\sigma$ or $\mathrm{Var}(x)$**. For discrete distribution $p_i$, probability of $X$ being $x_i$
$$
\sigma^2 = \sum_{i=1}^n p_i (x_i - \mu)^2
$$
For continuous distribution $f(x)$, probability of $X$ be in $(x, x+dx)$
$$
\sigma^2 = \int (x-\mu)^2 f(x)dx = \int x^2f(x)dx - \mu^2
$$
In general,
$$
\mathrm{Var}(x) = \langle x^2\rangle - \langle x \rangle ^2
$$
Properties:
 - $\mathrm{Var}(ax) = a^2 \mathrm{Var}(x)$
 - $\mathrm{Var}(x+a) = \mathrm{Var}(x)$
 - $\mathrm{Var}(ax + by) = a^2 \mathrm{Var}(x) + b^2 \mathrm{Var}(y) + 2ab \mathrm{Cov}(x,y)$
 - $\mathrm{Var}(ax - by) = a^2 \mathrm{Var}(x) + b^2 \mathrm{Var}(y) - 2ab \mathrm{Cov}(x,y)$

### Covariance and Covariance matrix
covariance is the tendency in linear relationship
$$
\mathrm{Cov}(X,Y) = \langle(X-\langle X \rangle) (\overline{Y - \langle Y\rangle})\rangle = \langle X\bar Y\rangle - \langle X\rangle\langle\bar Y\rangle
$$
or in another notation (and assuming real)
$$
\mathrm{Cov}(x,y) = \int dxdy f(x, y)(x-\mu_x)(y - \mu_y)
$$
or
$$
\mathrm{Cov}(x,y) = \langle (x-\mu_x)(y - \mu_y)\rangle
$$the bar over means complex conjugate. $X, Y$ is called *independent* if $\text{cov}(X,Y)=0$

In 2-dimension, covariance matrix $\Sigma$ or $C$ is defined as
$$
\Sigma := \pmatrix{
\mathrm{var}(X) & \mathrm{cov}(X,Y)\\
\mathrm{cov}(Y,X) & \mathrm{var}(Y)
}
$$
Covariance matrices are naturally symmetric by definition. In general,
$$
C = \langle \boldsymbol{n} \boldsymbol{n}^T\rangle
$$

