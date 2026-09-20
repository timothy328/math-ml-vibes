# Optimization — Topic 1: Geometry, Convexity, and First-Order Methods

## Learning goals

You will formulate optimization problems, distinguish local from global
optima, recognize convex structure, and derive gradient-descent updates.

## Part 1 — Problem formulation and geometry

An optimization problem has an objective, decision variables, and constraints:

`minimize f(x) subject to x ∈ C`.

A local minimum beats nearby feasible points; a global minimum beats every
feasible point. A stationary point satisfies `∇f(x)=0`, but stationarity alone
does not distinguish minima, maxima, and saddles.

For twice-differentiable functions, the Hessian describes local curvature.
Positive definite Hessian implies strict local convexity near a stationary
point; an indefinite Hessian indicates saddle-like curvature.

## Part 2 — Convex sets and functions

A set `C` is convex when the line segment between any two points in `C` stays
in `C`. A function is convex when:

`f(θx+(1-θ)y) ≤ θf(x)+(1-θ)f(y)` for `θ∈[0,1]`.

For differentiable functions, convexity is equivalent to the first-order
supporting-plane inequality:

`f(y) ≥ f(x)+∇f(x)^T(y-x)`.

For twice-differentiable functions on a convex domain, a positive
semidefinite Hessian is sufficient for convexity. Every local minimum of a
convex function is global, though not necessarily unique.

## Part 3 — Gradients and gradient descent

The gradient points in the direction of steepest local increase under the
Euclidean norm. Taylor expansion gives:

`f(x-η∇f(x)) ≈ f(x)-η||∇f(x)||²`.

Gradient descent repeatedly applies `x_{k+1}=x_k-η∇f(x_k)`. The step size
controls stability. For an `L`-smooth convex objective, sufficiently small
constant step sizes provide convergence guarantees; excessively large steps
can oscillate or diverge.

## Part 4 — Constraints and ML connections

Equality constraints can be handled with Lagrange multipliers. For
`min f(x)` subject to `g(x)=0`, the Lagrangian is `L(x,λ)=f(x)+λg(x)`.
KKT conditions generalize this idea to inequalities.

Regularized regression, maximum likelihood, and neural-network training are
optimization problems. Always identify whether the objective is convex,
whether constraints are present, and what assumptions support your algorithm.

