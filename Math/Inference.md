From lecture notes of modern astrostatistics, Elena Sellentin
## Inference: from data to theory
$$
\boxed{
P(x) = \int d^n\theta\,P(x, \theta) = \int d^n\theta\,\mathcal{L}(x|\theta) \pi (\theta)
}
$$
where
- $\theta$ is the human theories
- $x$ is the data provided by nature
- Likelihood $\mathcal{L}(x|\theta):=P(x|\theta)$
- $\pi(\theta)$: prior probability of $\theta$


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
