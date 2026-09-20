# Assessment: Brownian Motion and Gaussian Processes

Complete all four problems. State distributions, conditioning information,
and simulation assumptions clearly. No solutions are provided.

## Problem 1 — Increment structure

Let $0\le s<t<u<v$ and define
$A=W_t-W_s$, $B=W_u-W_t$, and $C=W_v-W_u$.

1. Give the joint distribution of $(A,B,C)$.
2. Compute the distribution of $2A-B+3C$.
3. Find $\operatorname{Cov}(W_t,W_v-W_u)$.
4. Explain which statements depend specifically on Gaussianity and which follow
   from independent increments.

## Problem 2 — Conditional Brownian bridge

For $0<s<T$, condition on $W_T=a$.

1. Derive the conditional mean and variance of $W_s$.
2. Compute $\operatorname{Cov}(W_s,W_t\mid W_T=a)$ for $s<t<T$.
3. Describe the behavior as $s$ approaches $0$ and $T$.
4. Explain how you would simulate a conditioned path on a finite grid.

## Problem 3 — Gaussian-process regression

Let $f$ have zero-mean kernel
$k(s,t)=\exp(-(s-t)^2/2)$ and observations
$y=(1,-1)^T$ at inputs $0$ and $1$, with noise variance $1/4$.

1. Construct the training covariance matrix including noise.
2. Find the predictive mean and variance at $t_*=1/2$.
3. Explain the effect of increasing the noise variance.
4. Give one reason a squared-exponential kernel may be a poor model for a
   rough physical signal.

## Problem 4 — Itô calculation and Monte Carlo

Let $dX_t=\alpha X_t\,dt+\beta X_t\,dW_t$ with $X_0=x_0>0$.

1. Apply Itô's formula to $\log X_t$.
2. Use the result to write an exact simulation formula for $X_T$.
3. Derive $\mathbb E[X_T]$ and discuss why a naive Euler simulation can be
   biased for nonlinear functionals.
4. Design a Monte Carlo estimate for $P(\max_{0\le t\le T}X_t>K)$ and note
   one limitation of a finite grid.
