The 1-D gaussian probability distribution takes the form
$$
f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} \exp{\frac{(x-\mu)^2}{2\sigma^2}}
$$
the normalization prefactor $1/\sqrt{2\pi\sigma^2}$ is found by $\int^\infty_{-\infty} dx\, f(x) = 1$. This integral can be solved by a coordinate transformation to $(r,\theta)$ can calculating the square of this integral, see [[Gaussian integral]]. 

Often denoted as $\mathcal{N}(\mu, \sigma^2)$ or $\mathcal{G}(\mu,\sigma^2)$. 

![[3sigma.jpg]]

Properties:
- If $x\sim \mathcal{N}(\mu,\sigma^2)$, then $\mathrm{E}(x)=\mu$, $\mathrm{Var}(x) = \sigma^2$.
### Multivariate gaussian distribution 
$$
P(\mathbf{x}) = (2\pi)^{-k/2}\det (\boldsymbol\Sigma)^{-1/2} \, \exp \left( -\frac{1}{2} (\mathbf{x} - \boldsymbol\mu)^\mathrm{T} \boldsymbol\Sigma^{-1}(\mathbf{x} - \boldsymbol\mu) \right)
$$
