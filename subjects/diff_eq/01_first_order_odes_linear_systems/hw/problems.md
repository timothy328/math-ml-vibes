# Homework: First-Order ODEs and Linear Systems

Show your setup, not only a final formula. State intervals of validity and
interpret equilibria or eigenvalues when requested.

## Problem 1 — Separable growth

Consider $y'=2ty(1-y/3)$ with $y(0)=1$.

1. Find all equilibrium solutions.
2. Solve the IVP explicitly.
3. Determine the long-run limit and describe the sign of $y'$ for initial
   values in each of the intervals $y<0$, $0<y<3$, and $y>3$.

## Problem 2 — Integrating factor and forcing

Solve the IVP
$$
y'-\frac{2}{t}y=t^2,\qquad y(1)=0,\qquad t>0.
$$

1. Find an integrating factor.
2. Obtain $y(t)$ and verify it by substitution.
3. Identify which term is the transient and describe its behavior as
   $t\to\infty$.

## Problem 3 — Exactness and qualitative analysis

Let
$$
(2ty+e^t)\,dt+(t^2+3y^2)\,dy=0.
$$

1. Check whether the equation is exact.
2. Find an implicit solution through $(0,1)$.
3. For the autonomous equation $u'=u(2-u)$, classify both equilibria using a
   phase line and explain what happens for $u(0)=1/2$ and $u(0)=3$.

## Problem 4 — A two-dimensional linear system

Let
$$
\mathbf{x}'=
\begin{bmatrix}3&1\\1&3\end{bmatrix}\mathbf{x},\qquad
\mathbf{x}(0)=\begin{bmatrix}2\\0\end{bmatrix}.
$$

1. Find the eigenvalues and an eigenvector for each.
2. Solve for $\mathbf{x}(t)$.
3. Compute $\lim_{t\to-\infty}\mathbf{x}(t)$ and explain the forward-time
   stability of the origin.

## Problem 5 — Challenge: coupled forcing

Consider
$$
\mathbf{x}'=
\begin{bmatrix}0&1\\-2&-3\end{bmatrix}\mathbf{x}
\begin{bmatrix}e^{-t}\\0\end{bmatrix},\qquad
\mathbf{x}(0)=\begin{bmatrix}1\\0\end{bmatrix}.
$$

1. Eliminate one variable to derive a second-order ODE for $x_1$.
2. Solve the resulting IVP, including a particular solution for the forcing.
3. Recover $x_2$, and use the eigenvalues of the homogeneous matrix to explain
   the long-run behavior.
