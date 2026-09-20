# Homework Solutions: First-Order ODEs and Linear Systems

## Problem 1

The equilibria are $y=0$ and $y=3$. Separation gives
$$
\int\frac{dy}{y(1-y/3)}=\int 2t\,dt.
$$
Using partial fractions, $\log|y/(3-y)|=2t^2+C$. The initial condition gives
$y/(3-y)=\frac12e^{2t^2}$, hence
$$
y(t)=\frac{3e^{2t^2}}{2+e^{2t^2}}
=\frac{3}{1+2e^{-2t^2}}.
$$
It tends to $3$. Since $y'=2ty(1-y/3)$ for $t>0$, the phase-line signs are
positive on $(0,3)$, negative above $3$, and negative below $0$ (because then
$y<0$ and $1-y/3>0$). Thus $0$ is unstable and $3$ is asymptotically stable;
negative initial values move downward, while positive values below $3$ rise
toward $3$.

## Problem 2

Here $p(t)=-2/t$, so $\mu(t)=e^{\int-2/t\,dt}=t^{-2}$. Thus
$$
(t^{-2}y)'=1.
$$
Integrating and applying $y(1)=0$ gives $t^{-2}y=t-1$, or
$$
y=t^3-t^2.
$$
Indeed, $y'-2y/t=(3t^2-2t)-(2t^2-2t)=t^2$. The homogeneous transient would
be $Ct^2$; it grows rather than decays on $t>0$, so the equation is not
relaxing in the usual constant-coefficient sense.

## Problem 3

For $M=2ty+e^t$ and $N=t^2+3y^2$, we have $M_y=2t=N_t$, so the equation is
exact. Integrating $M$ with respect to $t$ gives
$$
\Phi(t,y)=t^2y+e^t+\psi(y).
$$
Matching $\Phi_y=t^2+\psi'(y)=N$ gives $\psi(y)=y^3$. Through $(0,1)$,
$\Phi(0,1)=e+1$, so the implicit solution is
$$
t^2y+e^t+y^3=e+1.
$$
For $u'=u(2-u)$, the sign is negative for $u<0$, positive for $0<u<2$, and
negative for $u>2$. Thus $u=0$ is unstable and $u=2$ is asymptotically
stable. The solution from $1/2$ rises toward $2$; the solution from $3$
decreases toward $2$.

## Problem 4

The eigenpairs are $(\lambda_1,v_1)=(4,(1,1)^T)$ and
$(\lambda_2,v_2)=(2,(1,-1)^T)$. Write
$(2,0)^T=c_1v_1+c_2v_2$, which gives $c_1=c_2=1$. Therefore
$$
\mathbf{x}(t)=e^{4t}\begin{bmatrix}1\\1\end{bmatrix}
+e^{2t}\begin{bmatrix}1\\-1\end{bmatrix}
=\begin{bmatrix}e^{4t}+e^{2t}\\e^{4t}-e^{2t}\end{bmatrix}.
$$
Both modes vanish as $t\to-\infty$, so the limit is the zero vector. Both
eigenvalues are positive, so the origin is unstable forward in time.

## Problem 5

The equations are $x_1'=x_2+e^{-t}$ and $x_2'=-2x_1-3x_2$. Since
$x_2=x_1'-e^{-t}$, differentiating and substituting gives
$$
x_1''+3x_1'+2x_1=2e^{-t}.
$$
The initial data are $x_1(0)=1$ and $x_1'(0)=1$. A particular solution is
$x_{1,p}=2e^{-t}$ (the operator at $e^{-t}$ has value $(-1)^2+3(-1)+2=0$,
so resonance actually requires $x_{1,p}=2te^{-t}$). Substitution yields
$x_{1,p}=2te^{-t}$. The homogeneous solution is
$C_1e^{-t}+C_2e^{-2t}$. From the initial conditions,
$C_1=1$ and $C_2=0$, so
$$
x_1(t)=(1+2t)e^{-t}.
$$
Then $x_2=x_1'-e^{-t}=-2te^{-t}$. The matrix eigenvalues are $-1,-2$,
so all homogeneous modes decay; the resonant forcing adds the factor $t$ but
$te^{-t}\to0$, and the complete solution tends to zero.
