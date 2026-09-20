# Assessment: Bayes Rule and Conjugate Inference

Complete all four problems. State modeling assumptions and distinguish
posterior uncertainty from predictive uncertainty. No solutions are provided.

## Problem 1 — Multi-hypothesis Bayes rule

Three sensors have prior reliability hypotheses $H_1,H_2,H_3$ with prior
probabilities $(0.2,0.5,0.3)$. For an observed alarm $A$, the likelihoods are
$(0.9,0.6,0.2)$.

1. Compute the evidence $P(A)$.
2. Find all three posterior probabilities.
3. Compute posterior odds $P(H_1\mid A)/P(H_2\mid A)$.
4. Explain how a second conditionally independent alarm would update the
   calculation if its likelihood vector were $(0.8,0.7,0.1)$.

## Problem 2 — Beta-Binomial inference

Let $\theta\sim\operatorname{Beta}(a,b)$ and observe $s$ successes in $n$
trials.

1. Derive the normalized posterior density.
2. Derive the posterior predictive probability of exactly $r$ successes in
   $m$ future trials.
3. Evaluate the posterior mean, variance, and predictive probability when
   $(a,b,s,n,r,m)=(3,2,8,12,2,4)$.

## Problem 3 — Normal-normal prediction

Suppose $x_i\mid\mu\sim\mathcal N(\mu,\sigma^2)$ and
$\mu\sim\mathcal N(\mu_0,\tau_0^2)$, with all hyperparameters known.

1. Complete the square to derive the posterior precision and mean.
2. Derive the joint posterior predictive covariance of two future observations.
3. For $\sigma^2=1$, $\tau_0^2=4$, $n=4$, $\bar x=3$, and $\mu_0=1$, compute
   the posterior and the predictive correlation.

## Problem 4 — Decisions and posterior predictive checks

A medical model has posterior probability $q$ of a harmful condition. Action
$a=1$ treats and costs $c$ if the condition is absent; action $a=0$ has loss
$d$ if the condition is present.

1. Derive the Bayes action threshold in terms of $c$ and $d$.
2. Explain why a posterior predictive check can reveal poor calibration even
   when posterior intervals are narrow.
3. Design a simulation-based check using a maximum and a mean as discrepancy
   statistics, including what would count as evidence of mismatch.
