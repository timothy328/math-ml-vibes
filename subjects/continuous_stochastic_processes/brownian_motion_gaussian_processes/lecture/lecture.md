# Topic 1: Brownian Motion and Gaussian Processes

## Learning goals

This non-proof introduction treats a continuous-time stochastic process as a
random function $X_t$. You will work with Brownian motion, Gaussian
finite-dimensional distributions, increments, covariance, simulation, and the
intuition behind stochastic integration.

## Part 1 — Processes and finite-dimensional distributions

A stochastic process is a collection $\{X_t:t\ge0\}$ of random variables on a
common probability space. A sample path is one realized function of $t$.
Finite-dimensional distributions describe vectors
$(X_{t_1},\ldots,X_{t_k})$ for every finite set of times. Means and covariances
are
$$
m(t)=\mathbb E[X_t],\qquad C(s,t)=\operatorname{Cov}(X_s,X_t).
$$
For a Gaussian process, every finite vector is multivariate normal; its mean
function and covariance function determine all finite-dimensional
distributions. A covariance function must be symmetric and positive
semidefinite.

Stationarity can mean strict invariance under time shifts, or (in the
second-order sense used often here) constant mean and covariance depending only
on the lag $|t-s|$. Independent increments means increments over disjoint
intervals are independent; uncorrelated Gaussian increments are automatically
independent.

## Part 2 — Brownian motion

Standard Brownian motion $W_t$ satisfies $W_0=0$, has continuous sample paths,
independent increments, and
$$
W_t-W_s\sim\mathcal N(0,t-s)\quad(0\le s<t).
$$
Consequently $W_t\sim\mathcal N(0,t)$ and
$$
\operatorname{Cov}(W_s,W_t)=\min(s,t).
$$
For a drift-diffusion process $X_t=x_0+\mu t+\sigma W_t$,
$X_t\sim\mathcal N(x_0+\mu t,\sigma^2t)$ and increments over a length $h$
have mean $\mu h$ and variance $\sigma^2h$.

Brownian paths are continuous but extremely rough: typical increments have
size $\sqrt h$, not $h$. This explains why ordinary derivatives and
pathwise Riemann–Stieltjes calculations do not behave as in smooth calculus.

## Part 3 — Conditional laws and simulation

Because $(W_s,W_t)$ is jointly Gaussian, for $0<s<t$,
$$
W_t\mid W_s=x\sim\mathcal N(x,t-s).
$$
More generally, the conditional mean of a Gaussian vector follows the linear
regression formula $\mu_Y+\Sigma_{YX}\Sigma_{XX}^{-1}(x-\mu_X)$ and the
conditional covariance is $\Sigma_{YY}-\Sigma_{YX}\Sigma_{XX}^{-1}\Sigma_{XY}$.

On a grid $0=t_0<\cdots<t_n=T$, simulate independent
$Z_k\sim\mathcal N(0,1)$ and set
$$
W_{t_k}=W_{t_{k-1}}+\sqrt{t_k-t_{k-1}}\,Z_k.
$$
Adding drift and volatility gives $X_{t_k}=X_{t_{k-1}}+\mu\Delta t+
\sigma\sqrt{\Delta t}Z_k$. Finer grids improve visual resolution, not the
roughness of the ideal path.

## Part 4 — Gaussian processes beyond Brownian motion

A Gaussian process is specified by $m(t)$ and $C(s,t)$. A common example is
the squared-exponential kernel
$$
C(s,t)=\alpha^2\exp\left(-\frac{(s-t)^2}{2\ell^2}\right),
$$
where $\ell$ controls correlation length. Given noisy observations
$y_i=f(t_i)+\varepsilon_i$ with $\varepsilon_i\sim\mathcal N(0,\sigma_n^2)$,
the predictive mean and covariance at test inputs use
$$
\mu_* = K_{*X}(K_{XX}+\sigma_n^2I)^{-1}\mathbf y,\quad
\Sigma_* = K_{**}-K_{*X}(K_{XX}+\sigma_n^2I)^{-1}K_{X*}.
$$
This is the Gaussian-process regression analogue of conditioning a multivariate
normal.

## Part 5 — Itô intuition

For a smooth function, a Taylor expansion has first-order term
$f'(X_t)dX_t$ and a second-order term that is usually negligible. Brownian
increments satisfy $(dW_t)^2\approx dt$, so the second-order term survives.
Itô's formula for $f(t,X_t)$ when
$dX_t=a(t,X_t)\,dt+b(t,X_t)\,dW_t$ is
$$
df=f_t\,dt+f_x\,dX_t+\frac12f_{xx}b^2\,dt.
$$
The extra term is the core correction, not a technicality. The Itô integral is
defined from left-endpoint sums; for adapted integrands it has mean zero and
variance
$$
\mathbb E\left[\left(\int_0^T H_t\,dW_t\right)^2\right]
=\mathbb E\int_0^T H_t^2\,dt.
$$
Use these formulas for intuition and calculation, without treating $dW/dt$ as
an ordinary derivative.
