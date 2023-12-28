#### Continuity of functions
https://en.wikipedia.org/wiki/Continuous_function
- Epsilon-delta (Weierstrass and Jordan) definition -- a special case for real functions
- **Definition in terms of neighbourhoods** -- the general definition
$$ 
\boxed{
\begin{align}
&\qquad\text{A function $f:X \rightarrow Y $ is continuous at at point $x\in X$ }\\
&\text{if and only if for any neighbourhood $V$ of $f(x)$ in $Y$, there }\\
&\text{is a neighbourhood $U$ of $x$ such that $f(U) \subseteq V$. }
\end{align}
}
$$
Other facts
- $C^p$ continuous: $p$-th derivative exists and is continuous.
- Smooth is $C^\infty$ continuous: infinitely differentiable.

#### Taylor expansion
$$
f(x) = \sum_{n=0}^\infty \frac{1}{n!}f^{(n)}(x_0) (x-x_0)
$$
Some useful Taylor expansions and their radii of convergence
$$
\frac{1}{1-x} = 1 + x + x^2 + x^3 + \cdots, \forall x \in [-1,1]
$$
$$
e^x = \sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + x^2/2 + x^3/6 + \cdots, \forall x \in \mathbb{C} \text{ by def}
$$
$$
(1 + x)^\alpha = 1 + \alpha x + \frac{1}{2} \alpha(\alpha-1) x^2 + \cdots
$$
#### Fourier Transform
$$
\tilde f = \int_{-\infty}^{\infty}\frac{d^3k}{(2\pi)^{3/2}}fe^{-i\vec k\cdot \vec x}
$$

#### Special Integrals
$$
\int e^{i\vec k\cdot \vec x}d^3x = (2\pi)^3\delta(\vec k)
$$
### Gaussian Integral
$$
\int^\infty_{-\infty} e^{-x^2}dx = \sqrt \pi
$$
$$\int^\infty_{-\infty} e^{-fx^2+gx}dx = \sqrt{\frac{\pi}{f}}\exp\left(\frac{g^2}{4f}\right)$$
To calculate the Gaussian integral, consider the square of a Gaussian and integrate in polar coordinate $(r,\theta)$. Set
$$
I = \int\mathrm{d}x\, e^{-x^2}
$$
then consider the double integral $I^2$
$$
\int \,\mathrm{d}x\,\mathrm{d}y\, e^{-(x^2+y^2)} = \int \mathrm{d}r\,\mathrm{d}\theta\,re^{-r^2} = 2\pi\int\mathrm{d}r\,e^{-r^2} = \pi\int\mathrm{d}r^2\,e^{-r^2} = \pi
$$
Hence
$$
I = \sqrt{\pi}
$$
