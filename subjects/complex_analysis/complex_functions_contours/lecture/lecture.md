# Topic 1: Complex Arithmetic, Analytic Functions, and Contours

## Learning goals

You will work fluently with complex numbers, recognize holomorphic functions
through the Cauchy–Riemann equations, and evaluate simple contour integrals.
The geometric viewpoint is essential: complex differentiation is a stronger
condition than differentiability in one real direction.

## Part 1 — Complex numbers and geometry

Write $z=x+iy$ with $x,y\in\mathbb R$ and $i^2=-1$. The conjugate is
$\bar z=x-iy$, the modulus is $|z|=\sqrt{x^2+y^2}$, and
$z\bar z=|z|^2$. If $z\ne0$, then
$$
\frac{1}{z}=\frac{\bar z}{|z|^2}.
$$
In polar form, $z=re^{i\theta}=r(\cos\theta+i\sin\theta)$ with
$r=|z|$ and $\theta=\arg z$ modulo $2\pi$. Products multiply moduli and add
arguments; quotients divide moduli and subtract arguments. De Moivre's formula
is $(re^{i\theta})^n=r^ne^{in\theta}$.

The $n$th roots of $w=Re^{i\phi}$ are
$$
z_k=R^{1/n}e^{i(\phi+2\pi k)/n},\qquad k=0,\ldots,n-1.
$$
They form a regular polygon. The exponential is
$e^{x+iy}=e^x(\cos y+i\sin y)$ and is periodic in the imaginary direction:
$e^{z+2\pi i}=e^z$.

## Part 2 — Complex functions and limits

A function $f:\mathbb C\to\mathbb C$ is continuous at $z_0$ when
$f(z)\to f(z_0)$ as $|z-z_0|\to0$, independently of the path. The complex
derivative is
$$
f'(z_0)=\lim_{h\to0}\frac{f(z_0+h)-f(z_0)}{h},
$$
where $h$ may approach zero from every direction. Polynomials and power
series can be differentiated term by term inside their radius of convergence;
$e^z$, $\sin z$, and $\cos z$ are entire.

Write $f(z)=u(x,y)+iv(x,y)$. A quick path test can disprove a limit by taking
two approaches, such as $y=0$ and $x=0$. For derivatives, dependence on the
direction of $h$ signals failure even if partial derivatives exist.

## Part 3 — Cauchy–Riemann equations

If $u,v$ have continuous first partial derivatives near $(x_0,y_0)$, then a
necessary and sufficient condition for complex differentiability at that point
is
$$
u_x=v_y,\qquad u_y=-v_x.
$$
When these equations hold, $f'(z)=u_x+iv_x=v_y-iu_y$. If they hold throughout
an open set and the partial derivatives are continuous, $f$ is analytic
(holomorphic) there. Analyticity is an open-set property; checking one point
does not establish analyticity on a region.

For $f(z)=z^2$, $u=x^2-y^2$ and $v=2xy$, and the equations hold everywhere.
For $f(z)=\bar z$, $u=x,v=-y$, and they fail everywhere. A function can be
real-differentiable as a map $\mathbb R^2\to\mathbb R^2$ without being
complex-differentiable.

## Part 4 — Contours and line integrals

A parametrized contour is $\gamma:[a,b]\to\mathbb C$. For continuous $f$,
the contour integral is
$$
\int_\gamma f(z)\,dz=\int_a^b f(\gamma(t))\gamma'(t)\,dt.
$$
Reversing orientation changes the sign, and concatenating paths adds
integrals. If $\gamma(t)=z_0+tv$ is a line segment, this definition becomes
an ordinary real integral.

For a closed contour, $\oint_\gamma f(z)\,dz$ uses positive (counterclockwise)
or negative orientation. If $f=F'$ for an analytic primitive $F$ on a region
containing the path, the fundamental theorem gives
$\int_\gamma f(z)\,dz=F(\gamma(b))-F(\gamma(a))$, hence every closed integral
is zero. This is the practical content of path independence.

## Part 5 — Cauchy's theorem in basic form

If $f$ is analytic on and inside a closed, piecewise smooth contour $\gamma$
and the interior has no holes, then
$$
\oint_\gamma f(z)\,dz=0.
$$
The hypothesis matters: $1/z$ is analytic away from zero, but
$\oint_{|z|=1}dz/z=2\pi i$ because the contour encloses its singularity.
For elementary work, parameterize circles by $z=ae^{it}$, $0\le t\le2\pi$,
with $dz=iaz\,dt$, or use a primitive when one is available.

