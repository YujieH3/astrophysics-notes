Cartisian coordinates $(\vec{i},\vec{j},\vec{k})^T$ becomes $(\vec{i'},\vec{j'},\vec{k'})^T$ after linear transformation $R$. For any vector in space $\vec x$ we have

$$
\vec x
=(x',y',z')
\begin{pmatrix}
\vec i'\\
\vec j'\\
\vec k'
\end{pmatrix}
=
(x',y',z')L
\begin{pmatrix}
\vec i\\
\vec j\\
\vec k
\end{pmatrix}
=
(x,y,z)
\begin{pmatrix}
\vec i\\
\vec j\\
\vec k
\end{pmatrix}.
$$

This is to say, linear transformation  can be regarded either as a transformation of the vector coordinates or a transformation of the coordinates, depends on what you want to do.

This way the components of the same vector $\vec x$ in new coordinates is given by

$$(x',y',z') = (x,y,z)L^{-1}$$

The transposed form of above equations are used more often for the form of components transformation is easier

$$ \vec x = (\vec i', \vec j', \vec k')
\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
=
(\vec i, \vec j, \vec k)L^{T}
\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
=
(\vec i, \vec j, \vec k)
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}.
$$

It follows that 

$$
LL^T
\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
=
L
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}.
$$
If $L$ is orthogonal transformation (orthogonal matrix) then

$$\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
=
L
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix},$$

which is the formula in 《天文学教程》and《球面天文学》.

## Orthogonal Matrix
A matrix $A$ is called orthogonal if

$$A^{T} = A^{-1}$$