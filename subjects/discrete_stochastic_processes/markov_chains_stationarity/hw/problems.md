# Homework: Markov Chains, Transition Matrices, and Stationarity

Use row-vector distributions unless a problem explicitly asks for another
convention. Verify probabilities sum to one.

## Problem 1 — Two-state chain

Let
$$
P=\begin{bmatrix}0.8&0.2\\0.3&0.7\end{bmatrix},\qquad \pi_0=(1,0).
$$

1. Find $\pi_1$ and $\pi_2$.
2. Find the stationary distribution.
3. Compute the probability of state 2 at time 3.
4. Explain why the initial distribution's effect decreases here.

## Problem 2 — Path probabilities and classification

For
$$
P=\begin{bmatrix}1&0&0\\0.4&0.4&0.2\\0&0.5&0.5\end{bmatrix},
$$
with $X_0=2$:

1. Find the probability of the path $2,3,2,3$.
2. Identify absorbing, transient, and closed states or classes.
3. Find the probability of absorption in state 1 by time 2.
4. Explain whether a unique stationary distribution should be expected.

## Problem 3 — Three-state stationarity

Let
$$
P=\begin{bmatrix}0.5&0.5&0\\0.2&0.5&0.3\\0&0.4&0.6\end{bmatrix}.
$$

1. Solve for the stationary distribution.
2. Check it by multiplication.
3. Starting from state 1, compute the expected indicator of state 3 after one
   step and after two steps.
4. Describe why the positive diagonal entries matter for convergence.

## Problem 4 — Simulation design

Design a simulation for a four-state customer lifecycle chain with a given
transition matrix $P$ and initial distribution $\pi_0$.

1. Give precise pseudocode for one trajectory of length 100.
2. Give an estimator for $P(X_{10}=4)$ using 50,000 independent trajectories.
3. Give a different estimator for the stationary probability of state 4 using
   one trajectory with burn-in 1,000 and 100,000 recorded steps.
4. Identify one source of bias and one source of variance for each estimator.

## Problem 5 — Challenge: absorbing chain

Consider
$$
P=\begin{bmatrix}
1&0&0\\
0.2&0.5&0.3\\
0&0.4&0.6
\end{bmatrix}.
$$

1. Compute the absorption probability in state 1 starting from states 2 and 3.
2. Find the expected number of visits to transient states before absorption.
3. Compute the expected absorption time from each transient state.
4. Check one result by a first-step recursion.
