From [Parseval's theorem](https://en.wikipedia.org/wiki/Parseval%27s_theorem) and [Plancheral theorem](https://en.wikipedia.org/wiki/Plancherel_theorem)
That is, if $f(x)$ is a function on the real line, and $\hat f(\xi)$ is its frequency spectrum, then
$$
\int^\infty_{-\infty}|f(x)|^2 dx = \int^\infty_{-\infty}|\hat f(\xi)|^2 d\xi
$$
The unitarity of the Fourier transform is often called **Parseval's theorem** in science and engineering fields, based on an earlier (but less general) result that was used to prove the unitarity of the Fourier series.

### Other forms
Alternatively, for the discrete Fourier transform (DFT), the relation becomes:
$$
\sum^{N-1}_{n=0}|x[n]|^2 = \frac{1}{N}\sum^{N-1}_{k=0}|X[k]|^2
$$
When $X[k]$ is the DFT of $x[n]$
$$
X[k] = \sum^{N-1}_{n=0} x[n]\exp\left(-i\frac{2\pi}{N}kn\right)
$$

Proof
$$
\begin{align}
\frac{1}{N}\sum^{N-1}_{k=0}|X[k]|^2 &= \frac{1}{N}\sum^{N-1}_{k=0}X[k]\cdot X^*[k]\\
&= \frac{1}{N}\sum^{N-1}_{k=0}\left[ \sum^{N-1}_{n=0} x[n]\exp\left(-i\frac{2\pi}{N}kn\right) \right] X^*[k]\\
&= \frac{1}{N}\sum^{N-1}_{n=0} x[n] \left[ \sum^{N-1}_{k=0} X^*[k]\exp\left(-i\frac{2\pi}{N}kn\right) \right] \\
&= \frac{1}{N} \sum^{N-1}_{n=0} x[n](N\cdot x^*[n])\\
&= \sum^{N-1}_{n=0}|x[n]|^2
\end{align}
$$
Q.E.D.


A python script to verify Plancheral theorem. See [[Velocity Power Spectra#Appendix B Fourier Transform in np fft and in physics]] about the impletation of DFT in Numpy.

```python
import numpy as np
N = 50
f = np.random.rand(N,N,N)
g = np.fft.fftn(f)
print(1/N**3 * np.sum(np.abs(g)**2))
print(np.sum(f**2))
```

or

```python
```python
import numpy as np
N = 50
f = np.random.rand(N,N,N)
g = np.fft.fftn(f, norm="ortho")
print(np.sum(np.abs(g)**2))
print(np.sum(f**2))
```

You will find the two quantity printed here will be equal (with a little error).