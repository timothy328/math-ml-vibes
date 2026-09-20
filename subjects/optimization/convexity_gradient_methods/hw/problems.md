# Optimization — Topic 1 Homework

## Problem 1 — Quadratic geometry (Easy)

Let `f(x)=x^2-4x+7`.

1. Compute `f'(x)` and `f''(x)`.
2. Find the stationary point.
3. Classify it and compute the minimum value.
4. Rewrite `f` by completing the square.

## Problem 2 — Convexity (Easy)

For `f(x)=x^4`:

1. Compute the second derivative.
2. Determine where the second-derivative test proves convexity.
3. Show directly that `x=0` is a global minimum.
4. Explain why a stationary point is not automatically a minimum for every
   differentiable function.

## Problem 3 — Gradient descent (Medium)

Let `f(x)=1/2 x^T A x-b^T x`, where `A` is symmetric positive definite.

1. Derive `∇f(x)`.
2. Derive the stationary-point equation.
3. For `A=[[4,0],[0,2]]`, `b=[8,6]`, find the minimizer.
4. Write one gradient-descent update with step size `η`.

## Problem 4 — Lagrange multipliers (Medium)

Minimize `f(x,y)=x^2+y^2` subject to `x+y=1`.

1. Write the Lagrangian.
2. Derive the stationarity equations.
3. Solve for the optimizer and multiplier.
4. Explain geometrically why the solution is closest to the origin.

## Problem 5 — Conditioning and step size (Challenge)

Consider `f(x,y)=1/2(100x^2+y^2)`.

1. Compute the Hessian and its eigenvalues.
2. Explain why level sets are elongated.
3. Write the gradient-descent recurrence for both coordinates.
4. Determine a sufficient interval of constant step sizes for convergence.
5. Explain why rescaling the coordinates or preconditioning can help.

