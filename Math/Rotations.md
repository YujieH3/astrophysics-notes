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

## Rotation Matrix
$$R_x(\theta) = 
\begin{pmatrix}
1 & 0 & 0\\
0 & \cos\theta & \sin\theta\\
0 & -\sin\theta & \cos\theta\\
\end{pmatrix}
\qquad
R_y(\theta) = 
\begin{pmatrix}
\cos\theta & 0 & -\sin\theta\\
0 & 1 & 0\\
\sin\theta & 0 & \cos\theta\\
\end{pmatrix}
\qquad
R_z(\theta) = 
\begin{pmatrix}
\cos\theta & \sin\theta & 0\\
-\sin\theta & \cos\theta & 0\\
0 & 0 & 1\\
\end{pmatrix}
$$
- Rotational matrices are orthogonal matices: $R^T = R^{-1} = R(-\theta)$
- The different sign of $R_y$ is not a mistake, think about it. It follows the permutation: zxy, xyz, yzx (instead of yxz). 
- Multiplying rotation matrix to the right is rotating the vector by $-\theta$
$$
\boldsymbol{v}^TR_x(\theta) = [R_x(\theta)^T\boldsymbol{v}]^T = [R_x(-\theta) \boldsymbol{v}]^T
$$
