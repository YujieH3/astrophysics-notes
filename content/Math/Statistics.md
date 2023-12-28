### Expectation $E$, or Mean $\mu$, Variance $\sigma$
**Expectation $E$**. For discrete distribution $p_i$, probability of $X$ being $x_i$
$$
\mu = \sum^n_{i=1}p_ix_i
$$
**Mean $\mu$**. For continuous distribution $f(x)$, probability of $X$ be in $(x, x+dx)$
$$
\mu = \int xf(x)dx
$$
Mean $\mu$ is also called the *expectation* $E$ of $X$, namely $E(X)$.

**Variance $\sigma$**. For discrete distribution $p_i$, probability of $X$ being $x_i$
$$
\sigma^2 = \sum_{i=1}^n p_i (x_i - \mu)^2
$$
For continuous distribution $f(x)$, probability of $X$ be in $(x, x+dx)$
$$
\sigma^2 = \int (x-\mu)^2 f(x)dx = \int x^2f(x)dx - \mu^2
$$
### Covariance and Covariance matrix
covariance is the tendency in linear relationship
$$
\mathrm{cov}(X,Y) = \langle(X-\langle X \rangle) (\overline{Y - \langle Y\rangle})\rangle = \langle X\bar Y\rangle - \langle X\rangle\langle\bar Y\rangle
$$
the bar over means complex conjugate. $X, Y$ is called *independent* if $\text{cov}(X,Y)=0$

In 2-dimension, covariance matrix $\Sigma$ is defined as
$$
\Sigma := \pmatrix{
\mathrm{var}(X) & \mathrm{cov}(X,Y)\\
\mathrm{cov}(Y,X) & \mathrm{var}(Y)
}
= \pmatrix{
\sigma_X^2 & \rho\sigma_X\sigma_Y\\
\rho\sigma_X\sigma_Y & \sigma_Y^2
}
$$
Covariance matrices are naturally symmetric by definition. 

### Gaussian/Normal Distribution
A 1-dimensional normal distribution with variance $\sigma^2$ (standard variance $\sigma$), mean value $\mu$ is
$$g(x) = \frac{1}{\sigma\sqrt{2\pi}} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)$$
often denoted as $N(\mu, \sigma^2)$

![[3sigma.jpg]]
Where sigma is the variance.

## Likelihood, the probability (density) of observing our data given some parameter value
Therefore the integral $\int \mathcal{L(\theta)} d\theta$ does not necessarily $= 1$. Hence the "normalization" of likelihood over parameter space not only doesn't matter, but is also meaningless. 

See
[What is the difference between "likelihood" and "probability"?](https://stats.stackexchange.com/questions/2641/what-is-the-difference-between-likelihood-and-probability)
[What is the reason that a likelihood function is not a pdf?](https://stats.stackexchange.com/questions/31238/what-is-the-reason-that-a-likelihood-function-is-not-a-pdf)

For discrete data points $x_i$ and corresponding data $\tilde{x}_i(\theta)$ predicted by a model with parameters $\theta$, $\chi^2$ is defined as
$$\chi^2 = \sum_i\frac{(x_i - \tilde{x}_i)^2}{\sigma_i^2}$$
where $\sigma_i$ is the uncertainty in the measurement of $x_i$. (Not deviation from mean)

If the likelihood takes a Gaussian form (which is not always the case! but we use this all the time so beware!), the likelihood is related to $\chi^2$ in 
$$\mathcal{L}(\theta) = P(x|\theta) \propto \prod_i\exp\left[{-\frac{(x_i-\tilde{x}_i)^2}{2\sigma_i^2}}\right] = e^{-\frac{\chi^2}{2}}$$
$$\log\mathcal{L}(\theta)  \propto -\frac{\chi^2}{2}$$
Maximizing the likelihood is hence minimizing $\chi^2$. In parameter inference we can choose to maximize $\mathcal{L}$  or $\log\mathcal{L}$ or to minimize $\chi^2$ as we please. According to our problem and algorithm, some cases works better than others.

>**The likelihood is _not_ the probability of the parameter value being correct** or anything like that - **it is the probability (density) _of the data given the parameter value_**, which is a completely different thing. Therefore one should not expect the likelihood function to behave like a probability density.
