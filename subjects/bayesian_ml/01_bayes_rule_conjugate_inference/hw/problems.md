# Homework: Bayes Rule and Conjugate Inference

Show the likelihood, prior, and normalization or conjugate update used in each
answer. Use exact fractions when convenient.

## Problem 1 — Discrete Bayes rule

A rare condition has prevalence $P(H)=0.02$. A test has sensitivity
$P(+\mid H)=0.95$ and false-positive rate $P(+\mid H^c)=0.08$.

1. Compute $P(H\mid +)$.
2. Compute $P(H\mid -)$ using the same test.
3. Explain why a positive result does not imply a $95\%$ chance of disease.

## Problem 2 — Beta-Bernoulli learning

Let $\theta\sim\operatorname{Beta}(2,3)$ and observe ten Bernoulli trials with
seven successes.

1. Find the posterior distribution.
2. Compute its mean and mode.
3. Find the posterior predictive probability that the next two trials are both
   successes.
4. Compare the prior mean with the posterior mean and interpret the change.

## Problem 3 — Categorical prediction

A recommender has three click categories with prior
$\boldsymbol{\theta}\sim\operatorname{Dirichlet}(1,2,1)$. In 20 observations
the counts are $(8,5,7)$.

1. Write the posterior distribution.
2. Compute the predictive probability that the next category is category 2.
3. Compute the posterior expected click-share vector.
4. Explain the role of the concentration $\alpha_0+n$.

## Problem 4 — Gaussian posterior and decisions

Assume $x_i\mid\mu\sim\mathcal N(\mu,4)$, $\mu\sim\mathcal N(10,9)$, and
$n=9$ observations have $\bar x=12$.

1. Find the posterior mean and variance of $\mu$.
2. Find the posterior predictive distribution for one new observation.
3. Under squared-error loss, give the Bayes action for estimating $\mu$.
4. Compare the posterior uncertainty with the prior uncertainty.

## Problem 5 — Challenge: a decision threshold

A binary event has posterior probability $q=P(\theta=1\mid D)=0.3$. You can
either take action $a=1$ (intervene) or $a=0$ (do not intervene). The loss is
$L(1,0)=4$, $L(1,1)=1$, $L(0,0)=0$, and $L(0,1)=3$.

1. Derive both posterior risks as functions of $q$.
2. Find the threshold at which the optimal action changes.
3. Select the Bayes action for $q=0.3$ and $q=0.8$.
4. Describe how the threshold would change if intervention's false-positive
   loss increased.
