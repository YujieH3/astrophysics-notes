# Calculus for Physicists

Before talking at all about other concepts, it is important to add some remarks about the widely used Leibnitz notation. See [When can we not treat differentials as fractions? And when is it perfectly OK?](https://math.stackexchange.com/questions/1784671/when-can-we-not-treat-differentials-as-fractions-and-when-is-it-perfectly-ok) and [How misleading is it to regard 𝑑𝑦/𝑑𝑥 as a fraction?](https://mathoverflow.net/questions/73492/how-misleading-is-it-to-regard-fracdydx-as-a-fraction). The last question have more examples when this goes wrong. The practical summary is that $dy / dx$ looks like and works like a fraction in multiplication and division within first order, as a result of the chain rule. And $\partial y / \partial x$ almost never works like a fraction.

for example, these operations are correct
$$
\frac{dz}{dx} = \frac{dz}{dy} \frac{dy}{dx},\quad \frac{dy}{dx} = \frac{1}{dx / dy},\quad \frac{dy}{dx} = \frac{dz / dx}{dz / dy},\quad \frac{dx}{dx} = 1
$$
while these are not
$$
\frac{\partial y}{\partial x} = \frac{\partial z / \partial x}{\partial z / \partial y}, \quad
\left(\frac{dy}{dx}\right)^2 = \frac{dy^2}{dx^2} \quad\text{wrong!}
$$
The first one can be made correct with a negative sign
$$
\frac{\partial y}{\partial x} = - \frac{\partial z / \partial x}{\partial z / \partial y},
$$
and the second one is plain nonsense.

It is also fun / useful to check out [Most ambiguous and inconsistent phrases and notations in maths](https://math.stackexchange.com/questions/1024280/most-ambiguous-and-inconsistent-phrases-and-notations-in-maths)
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

#### Partial Derivative
[Partial derivatives with only one variable held constant](https://math.stackexchange.com/questions/3614200/partial-derivatives-with-only-one-variable-held-constant)
The rule of thumb is to make clear in partial derivative what is kept constant. For example, the partial derivative $\frac{\partial f}{\partial x}=1$ for $f(x,y,z) = x + 2y + 3z$ usually means to keep $y,z$ constant, regardless of further information how might $x$ depend on $y$ or $z$. If further down the line we know that $y$ is dependent on $x$ by $y=2x + 1$. Then $g(x,z) = f(x,y(x),z)$ would be a different function! In this case it is better to state explicitly (when it is unclear from context) if only $z$ is or both $y,z$ are kept constant when you write $\frac{\partial f}{\partial x}$. It is also tempting to ask how can $x$ variate without changing $y$? This is because we simply forget that fact that $y=2x+1$ when writing $f(x,y,z)$. 

Furthermore, $f(x,y,z)$ here by it self means nothing more than $f:\mathbb{R}^3 \rightarrow \mathbb{R}$, it is a map that takes a vector of three components and output a number. There is no 'dependence' whatsoever about components of the vector! Adding the information $y=2x+1$ later simply creates a new function, say $g:\mathbb{R}^2\rightarrow \mathbb{R}$, that has nothing to do with $f$. However the notation is often abused to keep calling this new function $f$, then you should be careful about what is kept constant to see whether the partial derivative of question is $\frac{\partial f}{\partial x}|_{y,z}=1$ or $\frac{\partial f}{\partial x}|_z=1 + 2\times2$. 

#### Taylor expansion
$$
f(x) = \sum_{n=0}^\infty \frac{1}{n!}f^{(n)}(x_0) (x-x_0)
$$
Some useful Taylor expansions and their radii of convergence
$$
\frac{1}{1-x} = 1 + x + x^2 + x^3 + \cdots, \forall x \in (-1,1)
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
[[Gaussian integral]]