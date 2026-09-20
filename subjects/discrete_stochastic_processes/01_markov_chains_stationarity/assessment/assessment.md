# Assessment: Markov Chains, Transition Matrices, and Stationarity

Complete all four problems. State your matrix convention and justify
classification claims. No solutions are provided.

## Problem 1 — Multi-step distribution

Let
$$
P=\begin{bmatrix}0.6&0.3&0.1\\0.1&0.7&0.2\\0.2&0.2&0.6\end{bmatrix},
\qquad \pi_0=(0.2,0.5,0.3).
$$

1. Compute $\pi_1$ and $\pi_2$.
2. Compute $(P^3)_{1,3}$ by matrix multiplication or path enumeration.
3. Find the stationary distribution.
4. Classify the chain and describe its long-run behavior.

## Problem 2 — Communicating classes

Consider
$$
P=\begin{bmatrix}
0.5&0.5&0&0\\
0&1&0&0\\
0.2&0&0.5&0.3\\
0&0&0&1
\end{bmatrix}.
$$

1. List all communicating classes and identify which are closed.
2. Identify transient and absorbing states.
3. For each starting state, describe the possible limiting distribution, if it
   exists.
4. Explain why a single global stationary distribution need not be unique.

## Problem 3 — Stationary expectations and dependence

Let an irreducible, aperiodic chain have stationary distribution $\pi$ and
state reward $r(i)$.

1. Express the stationary expected reward.
2. Explain the difference between the distribution of $r(X_n)$ and the
   long-run time average.
3. For a two-state chain with stationary mass $\pi_1=0.7$ and rewards
   $(2,-1)$, compute the stationary expected reward.
4. Describe why correlated samples affect standard-error calculations.

## Problem 4 — Simulation and validation

You are given a five-state transition matrix from an application.

1. Specify checks that validate it is a transition matrix.
2. Design an experiment comparing $\pi_0P^{50}$ with a one-chain empirical
   distribution after burn-in.
3. Give two diagnostics for a coding error in categorical sampling.
4. Explain how to report Monte Carlo uncertainty for an estimated state
   probability.
