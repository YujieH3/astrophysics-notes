- The determinant is a _multiplicative map_$\det(AB) = \det(A)\det(B)$
- Trace is invariant under circular shifts $\mathrm{Tr}(ABC) = \mathrm{Tr}(CBA) = \mathrm{Tr}(BCA)$

##### Diagonalizable matrix
In linear algebra, a square matrix $A$ is called diagonalizable or non-defective if it is similar to a diagonal matrix, i.e., if there exists an invertible matrix $P$ and a diagonal matrix $D$ such that $P^{-1} AP = D$, or equivalently $A= PDP^{-1}$ (such $P$, $D$ are not unique.)

##### Orthogonal matrix
In linear algebra, an orthogonal matrix is a real square matrix whose columns and rows are orthonormal vectors, or equivalently $Q^T Q = QQ^T = I$, or $Q^T=Q^{-1}$. 

- An orthogonal matrix is necessarily invertible, unitary ($Q^{-1}=Q^*$), and therefore normal ($Q^*Q = QQ^*$) over the real numbers. The determinant of any orthogonal matrix is either $+1$ or $-1$. 
- Real symmetric matrices are diagonalizable by orthogonal matrices. More generally, matrices are diagonalizable by unitary matrix if and only if they are normal.
##### Unitary matrix
In linear algebra, an invertible complex square matrix $U$ is unitary if its conjugate transpose $U^*$ is also its inverse, that is, if $U^* U = UU^* = UU^{-1} = I$.
##### Normal matrix
A complex square matrix $A$ is normal if it commutes with its conjugate transpose $A^*$, i.e. $A^*A=AA^*$.

- A matrix is normal if and only if it is unitarily similar to a diagonal matrix, and therefore any matrix $A$ satisfying the equation $A^*A=AA^*$ is diagonalizable. 

$A^*$ is the transposed conjugate of $A$. In quantum mechanics it is often called Hermitian adjoint and denoted as $A^\dagger$.
