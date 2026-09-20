# Optimization — Topic 1 Assessment

No solutions are provided for assessments.

## Problem 1 — Stationarity and curvature

Let $f(x,y)=x^2+4xy+5y^2-2x+6y$.

1. Compute the gradient and Hessian.
2. Find every stationary point.
3. Determine whether the Hessian is positive definite, semidefinite, or
   indefinite.
4. Classify the stationary point.
5. State whether the objective has a unique global minimizer.

## Problem 2 — Convexity and inequalities

Let $f(x)=\log(1+e^x)$.

1. Compute the first and second derivatives.
2. Prove convexity.
3. Write the first-order supporting-line inequality at an arbitrary point
   `x0`.
4. Explain one reason this function appears in classification models.

## Problem 3 — Constrained optimization

Minimize $x^2+2y^2+z^2$ subject to $x+y+z=1$ and $x\geq0$.

1. Write the Lagrangian for the equality constraint.
2. Solve the unconstrained equality-constrained problem.
3. Check whether the inequality constraint is active.
4. State the KKT conditions for the full problem.
5. Verify optimality using convexity.

## Problem 4 — Gradient descent analysis

For $f(x)=\frac12 x^\mathsf{T}Ax$, where $A$ is symmetric positive definite:

1. Derive the iteration matrix for gradient descent.
2. State a condition on `η` for convergence in terms of the largest
   eigenvalue.
3. Explain how the condition number affects convergence speed.
4. Compare fixed-step gradient descent with an exact line-search step for a
   quadratic.
5. Describe one practical diagnostic for detecting an unstable step size.
