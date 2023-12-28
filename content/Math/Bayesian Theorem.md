Application
[[Markov Chain Monte Carlo]]

Bayes' theorem is used in Bayesian methods to update probabilities, which are degrees of belief, after obtaining new data. Given two events $A$ and $B$, the conditional probability of $A$ given that $B$ is true is expressed as follows
$$
P(A|B) = \frac{P(A)P(B|A)}{P(B)}
$$
or
$$
P(A_i|B) = \frac{P(A_i)P(B|A_i)}{\sum_{k=1}^nP(A_k)P(B|A_k)}
$$
In a nutshell
$$\text{Posterior} = \frac{\text{Likelihood}\times\text{Prior}}{\text{Evidence}}$$
Symbol "$|$" means "given". 
## Bayesian Inference
Assume a signal $h$ buried in some data $d$. Probability that the signal has parameters $\vartheta = \{m_1, m_2,\dots\}$ is
$$p(\vartheta | d, h) = \frac{p(d|\vartheta, h)p(\vartheta|h)}{p(d|h)}$$

**Thoughts**
* *Likelihood*: The probability of observing the data assuming that a particular set of parameters is true.
* *Prior*: Represents our state of knowledge about the true parameters before measuring the data.
* *Posterior*: Represents our state of knowledge about the parameters after measuring the data.
$$p(\vartheta | x,f) = p(x - f(\vartheta)) = \prod_\lambda p(x_\lambda - f(\vartheta)_\lambda)$$
