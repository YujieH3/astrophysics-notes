[[Gravitational Wave]]
[[Black Hole]]

## A binary black hole signal

1. Inspiral
	analytically described by the post-Newtonian approximation
2. Merger
	Weak field approximation invalid. Numerical Relativity simulation required.
3. Ringdown (See [[Black Hole Ringdown]])
	Black hole *quasinormal modes*. "A black hole is completely described by its quasinormal modes, and the detection of a single quasinormal mode is sufficient to completely determine the spacetime of astrophysical black holes." 
	Fundamental quadrupolar mode - detected in 22 events.
	Secondary quasinormal mode
In analogy to the standard electromagnetic spectroscopy, the multimode analysis of the quasinormal modes is known as black hole spectroscopy.

The end state of astrophysical binary black hole (BBH) mergers is a perturbed single BH characterized by two parameters: the final remnant mass $M_f$ and spin angular momentum $S_f$.

A perturbed BH emit GW in three stages:
- The *transient* is the first stage and depends on the initial perturbation
- The *quasinormal modes* stage is the first stage and they are damped sinusoidal solutions. The amplitudes and phases of these modes are determined by the transient
- In the last stage the oscillattion ceases with a *power-law tail*

(Gravitational waves, Michele Maggiore)
The numerical simulations shows that, for an equal-mass non-spinning BH binary, the final BH mass and spin are
$$
\begin{align}
M_f &= (0.95162 \pm 0.00002)m\\
a_f &= (0.68646 \pm 0.00004)\frac{GM_f}{c^2}
\end{align}
$$
about $4.8\%$ of the total mass of the BBH is radiated away in GW. 


## Ringdown waveform: Quasinormal Modes (l,m,n)

The QNM frequencies are fully characterized by the remnant BH parameters, but their amplitudes and phases depend on the initial perturbation.
$$\omega_{lmn}\leftrightarrow{M, J, Q}$$
For a distant observer, the ringdown waveform written as the sum of the polarizations $+$ and $\times$ basis of the quasinormal modes is given by
$$h_++ih_\times = \frac{M_f}{r}\sum_{lmn}A_{lmn}\exp\{i[\omega_{lmn}(t-t_i)-\phi_{lmn}]\} _{-2}S_{lm}(a\omega_{lmn},\iota,\beta)$$
Where $_{-2}S_{lm}$ is spin-weighted spherical harmonics. The modes with $n=0$ are called *fundamental modes*, $n>0$ called the *overtones*.

*Harmonic mode* $(l,m)$ 
$$h_{lm} := \sum_n h_{lmn} := \sum_n A_{lmn}\exp{i[\omega_{lmn}(t-t_i)-\phi_{lmn}]}$$
- Most prominant $l=m=2$ harmonic $(2,2)$, *dominant mode* $(2,2,0)$
- Other strongest modes include $(3,3), (2,1), (4,4), (3,2)$
*For example, a nonspinning circular binary with mass ratio q = 1 does not excite the harmonics with odd m.* - But `gwsurrogate` does generate non-zero waveform for `mode_list = [(3,3)]`?
- higher overtones $n$ decay faster

[Black Hole Ringdown: The Importance of Overtones](https://link.aps.org/doi/10.1103/PhysRevX.9.041060) : 
The QNM frequencies are denoted $(\omega_{lmn}(M_f, \chi_f))$, where $l$ and $m$ describe the angular dependence of a mode and $n$, the often-ignored integer overtone index, sorts QNMs with the same angular dependence by how quickly they decay. The slowest decaying fundamental mode, $n=0$, is often considered to be of primary importance, while the more quickly decaying overtones are often disregarded. **However, we find that the overtones are not necessarily subdominant as is often assumed, but instead, they can dominate the early part of the ringdown.**
