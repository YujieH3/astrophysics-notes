#### Special Tensors
Kronecker delta 
$$
\delta^\mu_\rho = 
\left\{
\begin{aligned}
1, \mu = \rho,\\
0, \mu \neq \rho.
\end{aligned}
\right.
$$

Levi-Civita symbol 
$$
\tilde \epsilon_{\mu\nu\rho\sigma}=
\left\{
\begin{aligned}
&+1, &\mu\nu\rho\sigma\text{ is even permutation of 0123},\\
&-1, &\mu\nu\rho\sigma\text{ is odd permutation of 0123},\\
&0, &\text{two of the indices are equal.}
\end{aligned}
\right.
$$
#### Some comments on notations
$$
\begin{align}
X^{\mu}\,_{\nu} = X^{\mu\rho}g_{\rho\nu} = g_{\rho\nu}X^{\mu\rho} = \text{metric is always symmetric }
X^{\mu\rho}g_{\nu\rho} = g_{\nu\rho}X^{\mu\rho}
\end{align}
$$
The only thing you cannot move is the order of $\mu, \nu$, because $X$ is not necessarily symmetric.

Product of matrices: $(AB)_{\alpha\beta} = A_{\alpha\nu}B_{\nu\beta}$

In calculation, from Einstein summation to matrix multiplication, if you want: R(C-R)C. Index close to each other are summed over.

The inverse of $g_{\mu\nu}$ is $g^{\mu\nu}$. The definition is $g_{\mu\sigma}g^{\sigma\nu} = \delta^{\nu}_\mu$. 

#### Symmetry
Symmetric tensor $X^{\mu\nu} = X^{\nu\mu}$
Asymmetric tensor $X^{\mu\nu} = -X^{\nu\mu}$

the symmetric part of a (2,0) tensor $X^{(\mu\nu)} = \frac{1}{2}(X^{\mu\nu} + X^{\nu\mu})$
the asymmetric part of a (2,0) tensor $X^{(\mu\nu)} = \frac{1}{2}(X^{\mu\nu} - X^{\nu\mu})$
Always there is $A^{(\mu\nu)}B_{[\mu\nu]}$

For tensor more than two dimensions, sum over all permutations
Symmetric $T^{(\alpha_1\alpha_2\cdots\alpha_n)} = \frac{1}{n!}\sum_\sigma T^{\sigma(\alpha_1\alpha_2\cdots\alpha_n)}$
Antisymmetric $T^{[\alpha_1\alpha_2\cdots\alpha_n]} = \frac{1}{n!}\sum_\sigma (-1)^\sigma T^{\sigma(\alpha_1\alpha_2\cdots\alpha_n)}$

#### Tensor Calculus
Notation
$$\partial_\mu := \frac{\partial}{\partial x^\mu}, \partial^\mu = g^{\mu\nu}\frac{\partial}{\partial x^\nu} = \frac{\partial}{\partial x_\nu}$$