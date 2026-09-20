# Homework Solutions: Brownian Motion and Gaussian Processes

## Problem 1

An increment over length $h$ is $\mathcal N(0,h)$, so the first answers are
$0$ and $t-s$. Adjacent disjoint increments are independent, hence the
covariance is $0$. Since $W_2\sim\mathcal N(0,2)$,
$P(W_2>1)=1-\Phi(1/\sqrt2)$. Conditional on $W_1=0.5$,
$W_3-W_1\sim\mathcal N(0,2)$ and therefore
$W_3\mid W_1=0.5\sim\mathcal N(0.5,2)$.

## Problem 2

The mean is $4-0.7t$ and variance is $1.5^2t=2.25t$. The increment from 2 to
5 is $\mathcal N(-2.1,6.75)$. Also $X_5\sim\mathcal N(0.5,11.25)$, so
$P(X_5>0)=\Phi(0.5/\sqrt{11.25})\approx0.5297$. Increasing volatility
increases the spread; here, because the mean is positive, it moves more mass
below zero and reduces this probability toward $1/2$.

## Problem 3

The Gaussian conditional mean is $2+(1/4)(3-1)=2.5$, and conditional variance
is $9-1^2/4=35/4$. Thus $Y_2\mid Y_1=3\sim\mathcal N(2.5,35/4)$.
Using bilinearity,
$$
\operatorname{Cov}(Y_1+Y_2,Y_1-Y_2)
=\operatorname{Var}(Y_1)-\operatorname{Var}(Y_2)=4-9=-5.
$$
For jointly Gaussian variables, uncorrelatedness is equivalent to
independence because their joint density is determined by the covariance.

## Problem 4

Each step is
$X_{k+1}=X_k+0.4(0.01)+0.8\sqrt{0.01}Z_k$, with independent
$Z_k\sim\mathcal N(0,1)$. Initialize $X=2$, repeat this step 100 times, and
store the path. At $T=1$, the theoretical mean is $2.4$ and variance is
$0.64$. A finite Monte Carlo sample has sampling error, and finite-grid
discretization or implementation/rounding errors can add discrepancy (for
this constant-coefficient process the endpoint scheme itself has the exact
Gaussian endpoint law).

## Problem 5

With $f_x=2X_t$ and $f_{xx}=2$, Itô's formula gives
$$
d(X_t^2)=(2\mu X_t+\sigma^2)dt+2\sigma X_t\,dW_t.
$$
Integrating and taking expectations removes the stochastic integral:
$\mathbb E[X_T^2]=\mu^2T^2+\sigma^2T$. This equals
$(\mathbb E X_T)^2+\operatorname{Var}(X_T)=(\mu T)^2+\sigma^2T$.
Dropping $(dW)^2$ would omit the $\sigma^2dt$ term and incorrectly produce
only $\mu^2T^2$.
