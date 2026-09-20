# Assessment: First-Order ODEs and Linear Systems

Complete all four problems. Give exact answers where possible, justify
qualitative claims, and state any domain restrictions. No solutions are
provided in this file.

## Problem 1 — Autonomous IVP

Let $y'=y(1-y)(y+2)$ with $y(0)=y_0$.

1. Locate and classify all equilibria using a phase line.
2. Describe the solution's monotonicity and limiting behavior for
   $y_0=-3,-1,1/2,$ and $2$.
3. Separate variables and write an implicit solution for general
   $y_0\notin\{-2,0,1\}$.

## Problem 2 — Linear equation with a singular coefficient

For $t>0$, solve
$$
y'+\frac{3}{t}y=t^2\ln t,\qquad y(1)=2.
$$

1. Find the integrating factor and an explicit solution.
2. Verify the initial condition and substitution.
3. Determine the leading behavior as $t\to\infty$.

## Problem 3 — Exact differential and modeling

Consider
$$
(y\cos t+2t)\,dt+\left(\sin t+6y\right)\,dy=0.
$$

1. Test exactness and find a potential function.
2. Find the member of the family through $(0,1)$.
3. If $y$ represents a displacement, explain what information an implicit
   curve gives and when solving for $y(t)$ might fail globally.

## Problem 4 — Linear system and matrix exponential

Let
$$
\mathbf{x}'=
\begin{bmatrix}1&-2\\2&1\end{bmatrix}\mathbf{x}
\begin{bmatrix}e^t\\0\end{bmatrix},\qquad
\mathbf{x}(0)=\begin{bmatrix}0\\1\end{bmatrix}.
$$

1. Find the eigenvalues and describe the homogeneous trajectories.
2. Compute $e^{At}$ by writing $A=I+2J$ with $J^2=-I$.
3. Use variation of constants to express the solution and evaluate the
   integral.
4. Decide whether the forced solution is bounded as $t\to\infty$.
