# Topic 1: First-Order ODEs and Linear Systems

## Learning goals

By the end of this topic you should be able to classify and solve the main
first-order ordinary differential equations (ODEs), interpret equilibria and
stability, and use matrix exponentials or eigenvectors to solve a small
constant-coefficient linear system. An ODE describes an unknown function through
its derivatives; an initial condition selects one trajectory from a family.

## Part 1 — Modeling and separable equations

An ODE has the form
$F(t,y,y',\ldots,y^{(n)})=0$. The order is the highest derivative present.
For a first-order equation written as $y'=f(t,y)$, a solution is a function
whose graph follows the slope field. An initial-value problem (IVP) adds
$y(t_0)=y_0$.

If $y'=g(t)h(y)$, separate variables on an interval where $h(y)\ne0$:
$$
\frac{1}{h(y)}\,dy=g(t)\,dt.
$$
Integrate both sides, then use the initial condition. Do not discard constant
solutions found from $h(y)=0$. For example, for logistic growth
$$
y'=ry\left(1-\frac{y}{K}\right),
$$
the equilibria are $0$ and $K$. For $0<y_0<K$ the population rises toward
$K$; for $y_0>K$ it falls toward $K$.

For an autonomous equation $y'=f(y)$, equilibria satisfy $f(y_*)=0$. A phase
line made from the signs of $f$ gives qualitative behavior without solving:
arrows point right when $f(y)>0$ and left when $f(y)<0$. An equilibrium is
locally asymptotically stable if nearby solutions approach it.

## Part 2 — First-order linear equations

The standard linear form is
$$
y'+p(t)y=q(t).
$$
An integrating factor is
$$
\mu(t)=\exp\left(\int p(t)\,dt\right).
$$
Multiplying by $\mu$ turns the left side into
$(\mu y)'$, so
$$
\mu(t)y(t)=\int \mu(t)q(t)\,dt+C,\qquad
y(t)=\frac{\int \mu q\,dt+C}{\mu}.
$$
For an IVP, apply the initial condition after integrating (or use a definite
integral to reduce algebra):
$$
y(t)=\mu(t)^{-1}\left[\mu(t_0)y_0+
\int_{t_0}^{t}\mu(s)q(s)\,ds\right].
$$

The homogeneous equation $y'+p(t)y=0$ describes transients. A forcing term
$q(t)$ creates a particular response. In the constant-coefficient case
$y'+ay=b$, the equilibrium is $b/a$ when $a\ne0$, and
$y(t)=b/a+(y_0-b/a)e^{-a(t-t_0)}$.

## Part 3 — Exact equations and qualitative checks

An equation $M(t,y)\,dt+N(t,y)\,dy=0$ is exact if
$M_y=N_t$. Then there is a potential $\Phi$ with
$\Phi_t=M$ and $\Phi_y=N$, and solutions satisfy $\Phi(t,y)=C$. If the test
fails, an integrating factor depending only on $t$ or only on $y$ may exist.

Every proposed solution should be checked by differentiating and substituting.
A useful existence-and-uniqueness rule is: if $f$ and $\partial f/\partial y$
are continuous near $(t_0,y_0)$, then $y'=f(t,y)$ with $y(t_0)=y_0$ has a
unique local solution. Singularities in $f$ or in the resulting formula mark
the boundary of the interval on which that solution is valid.

## Part 4 — Linear systems and eigenmodes

Write a pair of first-order equations as
$$
\mathbf{x}'(t)=A\mathbf{x}(t)+\mathbf{g}(t),\qquad
\mathbf{x}(t)=\begin{bmatrix}x_1(t)\\x_2(t)\end{bmatrix}.
$$
For the homogeneous system, the fundamental matrix is
$e^{At}=\sum_{k=0}^{\infty}A^kt^k/k!$, and
$$
\mathbf{x}(t)=e^{A(t-t_0)}\mathbf{x}_0.
$$
If $A$ has independent eigenvectors $v_i$ with eigenvalues $\lambda_i$, then
$$
\mathbf{x}(t)=c_1e^{\lambda_1t}v_1+c_2e^{\lambda_2t}v_2.
$$
Constants come from the initial vector. Real eigenvalues give exponential
modes; a negative real part means decay, a positive real part growth, and
zero real part requires closer inspection. Complex eigenvalues produce
oscillations after taking real and imaginary parts.

For a forced system, variation of constants gives
$$
\mathbf{x}(t)=e^{A(t-t_0)}\mathbf{x}_0+
\int_{t_0}^{t}e^{A(t-s)}\mathbf{g}(s)\,ds.
$$
For a two-by-two matrix with repeated or non-diagonalizable eigenvalues, a
generalized eigenvector or the identity
$e^{At}=e^{\lambda t}e^{(A-\lambda I)t}$ is useful.

## Part 5 — A practical workflow

1. State the dependent and independent variables, domain, and initial data.
2. Classify the equation before manipulating it (separable, linear, exact, or
   system).
3. Solve symbolically, keeping equilibrium solutions and constants.
4. Use the initial condition and state the maximal interval justified by the
   formula.
5. Check by substitution and interpret signs, equilibria, time scales, and
   units. For systems, inspect eigenvalues before doing detailed algebra.

