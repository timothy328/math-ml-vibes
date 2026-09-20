# Optimization — Topic 1 Homework Solutions

## Problem 1

1. `f'=2x-4`, `f''=2`.
2. The stationary point is `x=2`.
3. Since `f''>0`, it is a strict global minimum; `f(2)=3`.
4. `f(x)=(x-2)^2+3`.

## Problem 2

1. `f''(x)=12x^2`.
2. It is nonnegative for every real `x`, so the second-derivative condition
   proves convexity everywhere.
3. `x^4≥0` for all `x`, with equality at zero.
4. A stationary point can be a maximum or saddle, as for `f(x)=-x^2` or
   `f(x)=x^3`.

## Problem 3

1. `∇f(x)=Ax-b` because `A` is symmetric.
2. `Ax=b`.
3. `x*=[2,3]`.
4. `x_{k+1}=x_k-η(Ax_k-b)`.

## Problem 4

1. `L=x^2+y^2+λ(x+y-1)`.
2. `2x+λ=0`, `2y+λ=0`, and `x+y=1`.
3. `x=y=1/2`, `λ=-1`.
4. The constraint is a line, and the closest point on that line to the origin
   lies where the radius is perpendicular to the line.

## Problem 5

1. The Hessian is `diag(100,1)` with eigenvalues 100 and 1.
2. Curvature is much greater in the x direction, producing elongated
   elliptical level sets.
3. `x_{k+1}=(1-100η)x_k` and `y_{k+1}=(1-η)y_k`.
4. Both factors must have magnitude less than 1, giving `0<η<1/50`.
5. Rescaling makes curvature more uniform, allowing a less restrictive
   step size and faster progress.

