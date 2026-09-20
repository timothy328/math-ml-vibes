# Homework: Brownian Motion and Gaussian Processes

Use covariance calculations and simulation reasoning explicitly. Proofs are not
required.

## Problem 1 — Brownian increments

Let $W$ be standard Brownian motion and $0<s<t<u$.

1. Find $\mathbb E[W_t-W_s]$ and $\operatorname{Var}(W_t-W_s)$.
2. Find $\operatorname{Cov}(W_t-W_s,W_u-W_t)$.
3. Compute $P(W_2>1)$.
4. Find the distribution of $W_3-W_1$ conditional on $W_1=0.5$.

## Problem 2 — Drift-diffusion

Let $X_t=4-0.7t+1.5W_t$.

1. Find the mean and variance of $X_t$.
2. Find the distribution of $X_5-X_2$.
3. Compute the probability that $X_5>0$.
4. Describe how changing the volatility affects this probability.

## Problem 3 — Gaussian conditioning

Suppose $(Y_1,Y_2)$ is jointly Gaussian with means $(1,2)$ and covariance
matrix $\begin{bmatrix}4&1\\1&9\end{bmatrix}$.

1. Find the law of $Y_2\mid Y_1=3$.
2. Find $\operatorname{Cov}(Y_1+Y_2,Y_1-Y_2)$.
3. Explain why zero covariance would imply independence in this setting.

## Problem 4 — Simulation and discretization

Use a grid with $\Delta t=0.01$ to simulate $T=1$ of
$X_t=2+0.4t+0.8W_t$.

1. State the increment formula and the distribution of each standard normal
   draw.
2. Give pseudocode or Python-like steps for one path.
3. Find the theoretical mean and variance at $T=1$.
4. Explain two sources of discrepancy between a sample average of 10,000
   simulated endpoints and the theoretical mean.

## Problem 5 — Challenge: Itô's formula

Let $X_t=\mu t+\sigma W_t$ and $f(x)=x^2$.

1. Use Itô's formula to derive $d(X_t^2)$.
2. Integrate and take expectations to find $\mathbb E[X_T^2]$.
3. Compare with the variance-plus-mean-squared calculation.
4. Explain why treating $(dW_t)^2$ as zero gives the wrong answer.
