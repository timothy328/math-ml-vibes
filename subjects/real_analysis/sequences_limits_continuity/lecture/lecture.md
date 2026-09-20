# Real Analysis — Topic 1: Sequences, Limits, and Continuity

## Learning goals

You will make informal notions of convergence precise, manipulate epsilon
arguments, use sequence tests, and connect continuity to numerical and ML
behavior.

## Part 1 — The real line and sequences

The real numbers are ordered and complete: every nonempty set bounded above
has a least upper bound. This completeness property distinguishes the reals
from the rationals and underlies convergence arguments.

A sequence is a function from the positive integers to the reals. It
converges to $L$ if for every $\varepsilon>0$ there exists $N$ such that
$n\geq N$ implies $|a_n-L|<\varepsilon$. The definition says that all
sufficiently late terms lie in every prescribed neighborhood of $L$.

Boundedness and monotonicity are useful but do not alone imply convergence.
A monotone bounded sequence does converge by completeness.

## Part 2 — Limits and epsilon proofs

The limit $\lim_{x\to a} f(x)=L$ means: for every $\varepsilon>0$, there
exists $\delta>0$ such that $0<|x-a|<\delta$ implies
$|f(x)-L|<\varepsilon$.

Proof workflow:

1. Start with the desired bound $|f(x)-L|<\varepsilon$.
2. Bound factors involving `x`.
3. Choose a neighborhood restriction and then choose $\delta$.
4. Verify the choices in forward order.

For products, sums, and compositions, limit laws reduce complex expressions
to known limits. Sequential characterization says the limit is $L$ exactly
when every sequence approaching `a` produces function values approaching `L`.

## Part 3 — Continuity and uniform continuity

$f$ is continuous at $a$ when $\lim_{x\to a}f(x)=f(a)$. Continuity preserves
limits under composition and ensures that a continuous function on a compact
interval attains its maximum and minimum.

Uniform continuity uses one $\delta$ for all points in a domain:

$$
|x-y|<\delta \Rightarrow |f(x)-f(y)|<\varepsilon.
$$

Every continuous function on a compact interval is uniformly continuous.
This is stronger than pointwise continuity and matters when a single error
tolerance must work across a dataset or parameter range.

## Part 4 — Analysis connections to data science

Lipschitz continuity, $|f(x)-f(y)|\leq K|x-y|$, gives a quantitative stability
guarantee. It supports robustness bounds and controls propagation of
approximation error. Convergence of iterative algorithms is often stated in
terms of sequences of parameter vectors or losses.

Do not confuse empirical convergence on a finite sample with a theorem about
all inputs. Analysis makes the quantifiers and domains explicit.
