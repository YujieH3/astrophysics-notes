For Laplace's equation
$$
\begin{align}
-\Delta u = f \quad \text{in}\,\Omega,\\
u = 0 \quad \text{on}\,\partial\Omega.
\end{align}
$$
Q1: What is a good way to approximate functions that requires only finitely much data/computation?
Q2: How do we find an approximation of the solution of a PDE without knowing the solution itself?

Approximation
1. (Finite) Fourier series
2. A global polynomial (Taylor series)
3. **Local (piecewise) polynomicals defined on a subdivision (the "mesh") of the domain $\Omega$**
4. ...

Commonly found features of solutions of PDEs:
- Smooth in large parts of the domain
- Vary greatly in small parts of the domain
- May have kinks
- Singularities in corners

Fourier approximation $u \approx \sum U_k\sin(kx)$ - localized kinks ruin the whole approximation
Taylor approximation $u \approx \sum U_k (x - x_0)^k$ - localized kinks ruin the whole approximation
	Weierstrass approximation theorem
	Every function $u(x)$ that is bounded on an interval $(a,b)$ can be approximated arbitrarily well by polynomials.
They work only if the function is smooth in $\Omega$

Solution: Piecewise approximation!
- Split the domain on which you want to approximate $u(x,y,\cdots)$ into small parts
- Approximate separately on each part
Advantages:
- We can use low-order approximations on each part
- Resolving kinks and singularities can be done locally
- We can increase the "resolution" where necessary - "(h-)adaptive mesh refinement (AMR)" - e.g. 10* cheaper in 2D, 100* cheaper in 3D
- We can increase the polynomial degree where the solution is smooth - "p-adaptive mesh refinement"

## Theory of piecewise polynomial approximation

Assume you have a function $f(x)$ on an interval $[a,b]$

It's "interpolant", say, $f_p(x)$:
- Also a function on $[a,b]$
- Has polynomial degree $p$
- Is equal to $f(x)$ at $(p+1)$ points $x_i$:
$$f_p(x_i) = f(x_i)\quad i=1,\cdots,p+1$$

HYJ: How to choose $x_i$?

**Theorem** (not optimal, but good enough):
Assume that $f$ is $p+1$ times continuously differentiable. Then independent of the choise of the points $x_i$
$$\max_{x\in[a,b]}|f(x)-f_p(x)| \leq \frac{\max_{x\in[a,b]}|f^{(p)}(x)|}{p!}(b-a)^p$$
$f^{(p)}(x)$ p-th derivative of $f(x)$
Read this as
$$\max_{x\in[a,b]}|f(x)-f_p(x)| \leq C(f,p)\frac{(b-a)^p}{p!}$$
Consequence:
- If $C(f,p)$ does not grow too quickly, then $\max_{x\in[a,b]}|f(x)-f_p(x)| \rightarrow 0$ as $p \rightarrow 0$
Problem: $f(x)=1/x$ on $[0.5,1.5]$
- **Polynomial approximant is not guaranteed to converge! (as $p$ increase)**

A better approach: keep $p$ constant and instead split the interval into $n$ pieces
**Theorem**: 
$$\max_{x\in[a,b]}|f(x)-f_{h,p}(x)| \leq \frac{C(f,p)}{p!}\left(\frac{b-a}{n}\right)^p = \frac{C(f,p)(b-a)^p}{p!}\frac{1}{n^p}$$
Consequence: Pick a $p$, choose enough intervals $n$, and you can make the difference as small as you want!

HYJ: "Assume that $f$ is $p+1$ times continuously differentiable" ... 

Denote the diameter of intervals/cells by $h$:
$$\max_{x\in[a,b]}|f(x)-f_{h,p}(x)| \leq \frac{C(f,p)}{p!}h^p$$

Two other estimates (also works in 2D and 3D):
L2-norm
$$
\Vert f-f_{h,p} \Vert :=\left(\int^b_a|f(x)-f_{h,p}(x)|^2\right)^{1/2}\leq \frac{C_1(f,p,a,b)}{p!}h^{p+1}
$$
Gradient norm / energy norm / h1 semi-norm
$$
\Vert \nabla f-\nabla f_{h,p} \Vert :=\left(\int^b_a|\nabla f(x)-\nabla f_{h,p}(x)|^2\right)^{1/2}\leq \frac{C_2(f,p,a,b)}{p!}h^{p}
$$
averaging difference of gradient

