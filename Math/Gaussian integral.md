The Gaussian integral takes the form
$$
\int^\infty_{-\infty} e^{-x^2}dx = \sqrt \pi
$$
$$\int^\infty_{-\infty} e^{-fx^2+gx}dx = \sqrt{\frac{\pi}{f}}\exp\left(\frac{g^2}{4f}\right)$$
$$
\int^\infty_{-\infty} e^{-\sigma x^2}dx = \sqrt \frac{\pi}{\sigma}
$$
**Proof:**
To calculate the Gaussian integral, consider the square of a Gaussian and integrate in polar coordinate $(r,\theta)$. Set
$$
I = \int\mathrm{d}x\, e^{-x^2}
$$
then consider the double integral $I^2$
$$
\int \,\mathrm{d}x\,\mathrm{d}y\, e^{-(x^2+y^2)} = \int \mathrm{d}r\,\mathrm{d}\theta\,re^{-r^2} = 2\pi\int r\mathrm{d}r\,e^{-r^2} = \pi\int\mathrm{d}r^2\,e^{-r^2} = \pi
$$
Hence
$$
I = \sqrt{\pi}
$$


## Imaginary width Gaussian integral
Gaussian integral with imaginary width is often used in Quantum physics, in the context of path integral. The Gaussian integral can be extended to imaginary width, as following,
$$
\int_{-\infty}^{\infty} d{x}\, e^{i\lambda x^2} =
    \sqrt{\frac{i\pi}{\lambda}},\quad \forall\lambda\in\mathbb{R}(\lambda\neq 0)
$$
The integral is proved by calculating the contour integral $\oint dz\,e^{i\lambda z^2} = 0$ along a trajectory involving a straight line on the real axis from $-\rho$


A calculation:
https://physics.stackexchange.com/questions/368186/gaussian-integral-with-imaginary-coefficients-and-wick-rotation