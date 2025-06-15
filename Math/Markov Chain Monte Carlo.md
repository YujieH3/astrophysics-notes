Based on [[Bayesian Theorem]]
In statistics, Markov chain Monte Carlo (MCMC) methods comprise a class of algorithms for sampling from a probability distribution. By constructing a Markov chain that has the desired distribution as its equilibrium distribution, one can obtain a sample of the desired distribution by recording states from the chain. The more steps that are included, the more closely the distribution of the sample matches the actual desired distribution. Various algorithms exist for constructing chains, including the Metropolis-Hastings algorithm.

https://youtu.be/yApmR-c_hKU
A sampling method.
* Markov Chain: next sample depends on last
* Monte Carlo: random sampling
After some burn-in samples, the samples after is (we wish) the stationary distribution, which has the desired probability distribution $p(x)$.

How to design the Markov Chain? Stationary distribution to be $p(x)$ $\leftarrow$ **detailed balance condition** $$p(x)T(y|x) = p(y)T(x|y)$$
Summing $x$ over both sides shows why this is the condition of stationary distribution
$$
\begin{align}
\sum_x p(x)T(y|x) = p(y) &= p(y)\sum_x T(x|y)\\
pT &= p
\end{align}
$$
where $T$ is the transition matrix. Notice $p(y)\sum_x T(x|y)$ is just the matrix multiplication.


## Metropolis-Hastings Algorithm
https://youtu.be/yCv2N7wGDCw
Function: to sample from $p(x)$ when we have only $f(x)$, where $p(x) = f(x)/N$, where $N$ is some normalizing factor. This is often the case in Bayesian inference. 
$$
p(\theta|x) = \frac{p(x|\theta)p(\theta)}{p(x)}
$$
where $p(x)$ is often infeasible.

1. Propose a sample according to $g(x_{t+1}|x_t)$
The next candidate is sampled from some distribution according to the previous candidate. e.g. The next candidate is sampled from a normal distribution centered on the previous candidate.
$$
g(x_{t+1}|x_t) = N(x_t, \sigma^2)
$$
The Metropolis algorithm refers to symmetric distribution here, and the Metropolis-Hastings algorithm is more general.
2. Accept to acceptance probability $A(x_t \rightarrow x_{t+1})$
The detailed balance condition, for any state $a, b$
$$
\begin{align}
P(a\rightarrow b) &= P(b\rightarrow a)\\
\frac{f(a)}{N}g(b|a)A(a\rightarrow b) &= \frac{f(b)}{N}g(a|b)A(b\rightarrow a)
\end{align}
$$
Therefore
$$
\frac{A(a\rightarrow b)}{A(b\rightarrow a)} = \frac{f(b)}{f(a)} \frac{g(a|b)}{g(b|a)} := r_fr_g
$$
if $r_f r_g < 1$, then $A(a\rightarrow b) = r_f r_g$, $A(b\rightarrow a) = 1$
if $r_f r_g \geq 1$, then $A(a\rightarrow b) = 1$, $A(b\rightarrow a) = 1/r_fr_g$

So
$$
A(a\rightarrow b) = \min\{1, r_f r_g\}
$$
This way the acceptance probability is set in such way that the transition probability in the constructed Markov chain will satisfy the detailed balance condition, i.e. the equilibrium condition. This is how the equilibrium distribution of the Markov chain can resemble the posterior.

For intuition, let $g$ be symmetric. Consider Metropolis algorithm
$$
A(a\rightarrow b) = \min\{1, {f(b)}/{f(a)}\} = \min\{1, {p(b)}/{p(a)}\}
$$
if $p(b)>p(a)$, then $A(a\rightarrow b) = 1$
if $p(b)< p(a)$, then $A(a\rightarrow b) = p(b)/p(a)$, the lower $p(b)$ is relative to $p(a)$, the less likely next sample will go there.

## Gibbs Sampling
https://youtu.be/7LB1VHp4tLE
Used when you want to sample 2 or more dimensional distribution. Use Gibbs sampling when sampling from $p(x,y)$ is difficult but sampling from $p(x|y)$, $p(y|x)$ is easy.

Procedure
1. Start at $(x^{(0)}, y^{(0)})$
2. Sample $x^{(1)} \sim p(x^{(1)}|y^{(0)})$
3. Sample $y^{(1)} \sim p(y^{(1)}|x^{(1)})$, then $(x^{(1)}, y^{(1)})$ is the next sample. 
4. go to 2 and repeat.

