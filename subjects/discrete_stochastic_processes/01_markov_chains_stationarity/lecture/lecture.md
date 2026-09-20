# Topic 1: Markov Chains, Transition Matrices, and Stationarity

## Learning goals

This topic introduces discrete-time stochastic processes whose next state
depends on the current state through a transition matrix. You will compute
multi-step probabilities, classify simple chains, find stationary
distributions, and simulate trajectories without proof-heavy Markov-chain
theory.

## Part 1 — Markov property and transition matrices

A discrete-time Markov chain $(X_n)_{n\ge0}$ on states
$\{1,\ldots,m\}$ satisfies
$$
P(X_{n+1}=j\mid X_n=i,X_{n-1},\ldots,X_0)
=P(X_{n+1}=j\mid X_n=i)=P_{ij}.
$$
The transition matrix $P$ has nonnegative entries and each row sums to one.
If the row vector $\pi_n$ gives the distribution of $X_n$, then
$$
\pi_{n+1}=\pi_nP,\qquad \pi_n=\pi_0P^n.
$$
The entry $(P^n)_{ij}$ is the probability of moving from $i$ to $j$ in $n$
steps. Matrix multiplication sums over all intermediate states.

An initial state is a point mass $e_i$; an initial distribution may represent
population uncertainty. Keep the row-versus-column convention consistent.

## Part 2 — Paths, classification, and absorbing behavior

A path probability is the initial probability times the product of transition
probabilities along the path. State $j$ is reachable from $i$ if some power
$P^n$ has positive $(i,j)$ entry. States communicating in both directions
form a communicating class. A state is absorbing when $P_{ii}=1$.

For finite chains, a closed class cannot be left. In an absorbing chain,
reordering transient states before absorbing states gives a block matrix
$$
P=\begin{bmatrix}Q&R\\0&I\end{bmatrix}.
$$
The fundamental matrix $N=(I-Q)^{-1}$, when it exists, records expected
visits to transient states; $NR$ gives absorption probabilities.

## Part 3 — Stationary distributions and long-run behavior

A stationary distribution is a probability row vector $\pi$ satisfying
$$
\pi P=\pi,\qquad \sum_i\pi_i=1,\quad\pi_i\ge0.
$$
Solve $(P^T-I)\pi^T=0$ plus normalization, or exploit balance equations.
Stationarity means that if $X_0\sim\pi$, every later $X_n$ has the same
distribution; it does not mean a single trajectory stays fixed.

A finite irreducible chain has one stationary distribution. If it also has
no periodic cycling (is aperiodic), distributions from any initial state
converge to it. A self-loop often makes a chain aperiodic. Periodic chains
may fail to converge even though a stationary distribution exists.

## Part 4 — Simulation and estimation

To simulate, draw $X_0$ from the initial distribution. Given $X_n=i$, draw
$X_{n+1}$ from row $P_{i,\cdot}$. Repeating trajectories estimates
probabilities by relative frequencies. For a long ergodic trajectory, the
fraction of visits to state $i$ estimates $\pi_i$, though adjacent
observations are dependent.

For reproducible numerical work, record the random seed, transition matrix,
initial law, number of steps, burn-in, and whether samples are independent
trajectories or one dependent path.

## Part 5 — A practical workflow

1. Check that $P$ is stochastic and label states clearly.
2. Compute one-step and multi-step distributions using $\pi_0P^n$.
3. Inspect reachability, closed classes, absorbing states, and self-loops.
4. Solve for stationary distributions and check nonnegativity and
   normalization.
5. Compare analytic results with a simulation and distinguish finite-sample
   fluctuation from a modeling or coding error.
