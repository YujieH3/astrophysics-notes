The main purpose of this page is for the discussion of [[General Relativity]]. 
Reference: Carroll (Spacetime and Geometry)
#### Manifold, an (union of) open set with compatible charts
An open ball $B_r(y)$ in $\mathbb{R}^n$: $|x-y|<r\in \mathbb{R}$ $\longrightarrow$ An open set $V\subseteq \mathbb{R}^n$: the arbitrary union of open balls / any point $y\in V$ can be the center of a open ball completely inside. 
A chart / coordinate system: subset $U \subset M$ plus a one-to-one map $\phi:U\rightarrow \mathbb{R}^n$, such that $\phi(U)$ is an *open* set (henceforth we can say $U$ is an open set in $M$). $\longrightarrow$ A $C^\infty$ atlas of set $M$: a collection of charts where the union of open sets is equal to $M$ and the maps are sewed smoothly together - where the translation (transformation) between every two charts are infinitely differentiable, i.e. $\forall \phi_\alpha:U_\alpha\rightarrow \mathbb{R}^n, \phi_\beta:U_\beta\rightarrow \mathbb{R}^n$, then $(\phi_\alpha\circ\phi_\beta^{-1}):\mathbb{R}^n\rightarrow \mathbb{R}^n,\in C^\infty$. 

Finally we define manifold
$$
\boxed{
\begin{align}
&\qquad\text{A $C^\infty$ n-dimensional manifold (n-manifold) is simply a}\\ 
&\text{set $M$ along with a maximal $C^\infty$ atlas, one that contains every}\\ 
&\text{possible compatible chart.}\end{align}
}
$$
Some remarks
- $C^\infty$ can be substitute with $C^p$ for definition of $C^p$ n-manifold. But we study smooth ($C^\infty$) ones here.
- $\phi(U)$ of a chart is required to be open. [Why do charts require open sets?](https://math.stackexchange.com/questions/2127756/why-do-coordinate-charts-require-open-sets) 
- The opening of $U$ is defined following the opening of $\phi(U)$.
- Despite a.k.a coordinate systems, charts differs from our usual notion of coordinate system by the requirement that $\phi(U)$ is open. E.g. the spherical coordinate system $(r\in[0,\infty), \theta\in[0,\pi], \phi\in[0,2\pi])$ is closed, and therefore not a chart. 
- I find the name "coordinate transformation" quite misleading. Changing your language of describing the same thing is not transformation, it should be called translation.

Examples of manifolds
- n-dimensional Euclidean space $\mathbb{R}^n$
- n-sphere $S^n$
- n-torus $T^n$
- two-torus with $g$ holes, Riemann surfaces of genus $g$

In GR, the smooth manifold is the spacetime itself. $(t,r,\theta,\phi)$ coordinate system is a chart in the  manifold. For example, Schwarzschild metric is a (0,2) tensor defined in the manifold. The coordinate singularity at $r=2M$ is merely a bad patch of our map which could be removed in [Kruskal-Szekeres coordinates](https://en.wikipedia.org/wiki/Kruskal–Szekeres_coordinates). The only singularity in this spacetime is the physical singularity at $r=0$. We can easily remove and have a perfect smooth manifold left. 

See this excellent question and answer [Coordinate singularity in general relativity and smooth structure of a manifold](https://physics.stackexchange.com/questions/705091/coordinate-singularity-in-general-relativity-and-smooth-structure-of-a-manifold)

#### Diffeomorphic, the "same" manifolds
$$
\boxed{
\begin{align}
&\qquad\text{Two sets M and N are called diffeomorphic if there exists}\\ 
&\text{a $C^\infty$ map $\phi:M\rightarrow N$ with a $C^\infty$ inverse $\phi^{-1}:N\rightarrow M$; The}\\
&\text{map $\phi$ is then called a diffeomorphism. }
\end{align}
}
$$
e.g. SO(2) and $S^1$ (1-sphere, circle) are diffeomorphic.

#### Vector, One-form, and Tensor, A bunch of objects on manifold

A curve is $\gamma: \mathbb{R} \rightarrow M$. A curve "parametrized by $\lambda$" simply means we denote the variable $\lambda\in\mathbb{R}$ as $\gamma(\lambda)$, and $\forall \lambda, \gamma(\lambda)=p\in M$, a number $\lambda$ corresponds to a point $p$ on the curve $\lambda$ in the manifold $M$. Sometimes when we say "a curve $x^\mu(\lambda)$", it means $x^\mu(\lambda) = (\phi\circ \gamma):\mathbb{R}\rightarrow M \rightarrow \mathbb{R}^n$, where a specific coordinate system is used. $x^\mu(\lambda)$ is a representation of a curve under a chosen coordinate system. Keep in mind that a curve itself is independent of coordinate choice. 

A function is $f:M\rightarrow \mathbb{R}$ (unless stated otherwise). Similar to the case of curve, $f(x^\mu)$ means $f(x^\mu)=(f\circ \phi^{-1}):\mathbb{R}^n\rightarrow M \rightarrow \mathbb{R}$. A function on a manifold is like a scalar field.

A vector at a point $p$ is defined as a directional derivative operator $\frac{d}{d \lambda}$. When acting on a function
$$
\frac{d }{d \lambda}f = \frac{d }{d \lambda}f(x^\mu (\lambda)) = \frac{dx^\mu}{d \lambda}\frac{\partial }{\partial x^\mu}f,
$$
meaning any vector can be decomposed in basis of $\partial_\mu$, i.e. $V = V^\mu\partial_\mu$, this choice of basis $\hat e_{(\mu)} = \partial_\mu$ is called a **coordinate basis**. There are also non-coordinate basis. A vector at $p$ maps a function at $p$ to a number, while a vector field maps a function ($M\rightarrow \mathbb{R}$) to a function ($M\rightarrow \mathbb{R}$).

A one-form $\omega: T_p\rightarrow \mathbb{R}$ can be expressed in term of the coordinate basis of one-forms: $\omega = \omega_\mu\mathrm{d}x^\mu$. The gradient of a function act on directional derivative operator as
$$
\mathrm{d} f\frac{d}{d \lambda} = \frac{df}{d\lambda}
$$
(easier to understand in Euclidean space $\nabla f \cdot \frac{df}{d\vec{v}} = \frac{df}{dv}$) The set of basis matches properly because $\mathrm{d}x^\mu\partial_\nu = \partial x^\mu / \partial x_\nu = \delta^\mu_\nu$.

A $(k,l)$ tensor
$$
T = T^{\mu_1\cdots\mu_k}\,_{\nu_1\cdots\nu_l} (\partial_{\mu_1}\otimes \cdots \otimes\partial_{\mu_k}\otimes\mathrm{d}x^{\nu_1}\otimes \cdots \otimes\mathrm{d}x^{\mu_k})
$$
#### The Metric, good honest (0,2) tensor

The (0,2) metric tensor $g = g_{\mu\nu}(\mathrm{d}x^\mu\otimes \mathrm{d}x^\nu)$, the basis is the [tensor product](https://en.wikipedia.org/wiki/Tensor_product) of two basis one-forms or basis dual vectors. But as $g$ is taken to represent the determinant of the metric. We use
$$
ds^2 = g_{\mu\nu}\mathrm{d}x^\mu\mathrm{d}x^\nu
$$
we call $ds^2$ "metric" and "line element" interchangeably. But keep in mind it is a tensor, written in components $\times$ basis. Also keep in mind $\mathrm{d}x^\mu\mathrm{d}x^\nu$ here is actually our honest (0,2) tensor $\mathrm{d}x^\mu\otimes \mathrm{d}x^\nu$, and $\mathrm{d}x^\mu\mathrm{d}x^\nu\neq \mathrm{d}x^\nu\mathrm{d}x^\mu$. (Tensor product does not commute)
#### Some other facts
- Any $n$-manifold can be embedded in $\mathbb{R}^{2n}$ (Whitney's embedding theorem)
- A Klein bottle is an example of a 2-manifold that cannot be embedded in $\mathbb{R}^{3}$
- "In principle, tensor components need not change when we change coordinates, they change when we change the basis in the tangent space, but we have decided to use the coordinates to define our basis. Therefore a change of coordinates induces a change of basis"
- "The word Euclidean sometimes means that the space is flat, and sometimes doesn't, but it always means that the canonical form is strictly positive; the terminology is unfortunate but standard."

> [! On dx notation ⚠️]
> Most references are not sufficiently picky to distinguish between "$dx$," the informal notion of an infinitesimal displacement, and "$\mathrm{d}x$" the rigorous notion of a basis one-form given by the gradient of a coordinate function. (They also tend to neglect the fact that tensor products don't commute, and write expressions like $\mathrm{d}x\mathrm{d}y + \mathrm{d}y\mathrm{d}x$ as $2\mathrm{d}x\mathrm{d}y$; it should be clear what is meant from the context.) In fact our notation "$ds^2$" does not refer to the differential of anything, or the square of anything; it's just conventional shorthand for the metric tensor, a multilinear map from two vectors to the real numbers." - Carroll
