1. Rotation is linear -> hence matrix representation
	1. $R(v+w) = R(v) + R(w)$
	2. $R(\lambda v) = \lambda R(v)$
2. Preserves lengths and angles -> preserve dot product
$$v^T w = (v^TR^T)(Rw) \implies R^TR=I$$
3. Preserves orientation $\det R =1$ 

In summary

| Properties of rotation | Real | Complex |
| ---------------------- | ---- | ------- |
| Rotation is linear     | Rotate$(v) = Rv$ | Rotate$(v) = Uv$ |
| Preserves lengths and angles | $R^TR = \mathbb{1} \Rightarrow O(n)$ | $U^\dagger U = \mathbb{1} \Rightarrow U(n)$ |
| Preserves orientation | $\det R = \mathbb{1}$ | $\det U = \mathbb{1}$ |
| All | $SO(n)$ | $SU(n)$ |

They are called the orthogonal or unitary matrices
$$
\boxed{
\begin{align}
R \in O(n) = \left\{R \text{ is } n\times n, R^TR=\mathbb{1}\right\}\\
R \in SO(n) = \left\{R\in O(n), \det R=1\right\}\\
\end{align}
}
$$
$$
\boxed{
\begin{align}
U \in U(n) = \left\{U \text{ is } n\times n, U^\dagger U=\mathbb{1}\right\}\\
U \in SU(n) = \left\{U\in O(n), \det U=1\right\}\\
\end{align}
}
$$



