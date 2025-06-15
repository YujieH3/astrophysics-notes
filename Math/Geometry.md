## Plane
For a plane $Ax + By + Cz + D = 0$, the normal vector of the plane is $\vec{n} = (A,B,C)/\sqrt{A^2+B^2+C^2}$. The plane equation can be rewritten as $A(x-x_0) + B(y-y_0) + C(z-z_0) = 0$, i.e. $\vec{n}\cdot (\vec{x}-\vec{x}_0)=0$, where $\vec{x}_0 = (x_0, y_0, z_0)$ is some point on the plane.

The distance of some point $\vec{x}_1 = (x_1, y_1, z_1)$ to a plane $Ax + By + Cz + D = 0$ is
$$d = \frac{|Ax_1 + By_1 + Cz_1 + D|}{\sqrt{A^2+B^2+C^2}}$$
Proof:
$$
\begin{align}
d &= |(\vec{x_1} - \vec{x_0})\cdot \vec{n}|\\
&= \frac{|A(x_1-x_0) + B(y_1-y_0) + C(z_1-z_0)|}{\sqrt{A^2+B^2+C^2}}\\
&= \frac{|Ax_1 + By_1 + Cz_1 - Ax_0 - By_0 - Cz_0|}{\sqrt{A^2+B^2+C^2}}\\
&= \frac{|Ax_1 + By_1 + Cz_1 + D|}{\sqrt{A^2+B^2+C^2}}
\end{align}
$$