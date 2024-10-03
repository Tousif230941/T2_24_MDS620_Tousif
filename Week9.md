
Variational Inference (VI) is a powerful technique for approximate inference in complex probabilistic models. Let me address your questions: </br>
Main goal of Variational Inference and comparison to MCMC:</br>
The main goal of Variational Inference is to approximate complex posterior distributions with simpler, tractable distributions. It aims to find the best approximation within a family of simpler distributions by minimizing the Kullback-Leibler (KL) divergence between the approximation and the true posterior.</br>
VI is often preferred over MCMC methods for several reasons:</br>
Speed: VI typically converges faster than MCMC, especially for large datasets.</br>
Scalability: VI can be more easily applied to large-scale problems.</br>
Deterministic: VI provides a deterministic optimization procedure, unlike the stochastic nature of MCMC.</br>
Easier to assess convergence: VI's optimization objective provides a clear measure of convergence.</br>
Variational distribution q(w):</br>
The variational distribution q(w) is the approximating distribution used to approximate the true posterior p(w|x). It is typically chosen from a family of simpler, tractable distributions (e.g., Gaussian) that can be easily optimized. The parameters of q(w) are adjusted to minimize the KL divergence between q(w) and the true posterior p(w|x).</br>
KL divergence in Variational Inference:</br>
The Kullback-Leibler (KL) divergence is a measure of the difference between two probability distributions. In VI, it's used to quantify how close the approximating distribution q(w) is to the true posterior p(w|x).</br>
KL divergence is defined as:</br>
KL(q||p) = ∫ q(w) log(q(w)/p(w|x)) dw</br>
VI aims to minimize this KL divergence, which is equivalent to maximizing the Evidence Lower Bound (ELBO).</br>
Two main components of the ELBO:</br>
The Evidence Lower Bound (ELBO) consists of two main components:</br>
a) Expected log-likelihood: E_q[log p(x|w)]</br>
This term encourages the approximation to explain the observed data well.</br>
b) KL divergence between q(w) and the prior p(w): -KL(q(w)||p(w))</br>
This term acts as a regularizer, encouraging the approximation to be close to the prior.</br>
The ELBO can be written as:</br>
ELBO = E_q[log p(x|w)] - KL(q(w)||p(w))</br>
Maximizing the ELBO with respect to the parameters of q(w) provides the best approximation to the true posterior within the chosen family of distributions.</br>
