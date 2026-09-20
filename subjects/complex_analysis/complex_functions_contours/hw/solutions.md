# Homework Solutions: Complex Arithmetic, Analytic Functions, and Contours

## Problem 1

We have $z+w=-1-\sqrt3i$ and
$zw=\sqrt3-2+(1+2\sqrt3)i$. Since $|w|^2=5$,
$$
\frac zw=\frac{(1-\sqrt3i)(-2-i)}5
=\frac{-2-\sqrt3}{5}+\frac{2\sqrt3-1}{5}i.
$$
The modulus of $z$ is $2$ and its argument is $5\pi/3$, so
$z=2e^{i5\pi/3}$. Its cube roots are
$$
2^{1/3}e^{i(5\pi/3+2\pi k)/3},\qquad k=0,1,2.
$$

## Problem 2

Along $z=x\in\mathbb R$ with $x\ne0$, $\bar z/z=1$; along $z=iy$ with
$y\ne0$, it is $-1$. The limit therefore does not exist. For the
polynomial, $f'(z)=3z^2-2$, so $f'(1+i)=-2+6i$. Real partial derivatives
only test coordinate directions; a complex derivative requires the same
quotient limit for every direction of $h$.

## Problem 3

For $z^2+\bar z$, $u=x^2-y^2+x$ and $v=2xy-y$. The equations would require
$2x+1=2x-1$, impossible; it is analytic nowhere. For $|z|^2$,
$u=x^2+y^2,v=0$, so the equations hold only at $(0,0)$; it is not analytic
on any open set. Finally, $e^x(\cos y+i\sin y)=e^z$, whose Cauchy–Riemann
equations hold everywhere, so it is entire and has derivative $e^z$.

## Problem 4

For $z^2$, a primitive is $F(z)=z^3/3$, so
$$
\int_\gamma z^2\,dz=\frac{(1+i)^3-1}{3}=\frac{-3+2i}{3}.
$$
For $z=t(1+i)$, $\bar z=t(1-i)$ and $dz=(1+i)dt$, hence
$\int_0^1 2t\,dt=1$. The polynomial $z^2+1$ has a primitive, so its circle
integral is zero. On $|z|=2$, $z=2e^{it}$ gives $dz/z=i\,dt$ and
$\oint dz/z=2\pi i$. The integrand has a singularity inside the circle.

## Problem 5

For the four sides, the integrals of $\bar z\,dz$ are respectively
$1/2$, $1/2+i$, $-1/2+i$, and $-1/2$, totaling $2i$. This agrees with
$\oint\bar z\,dz=2i$ times the enclosed area for this positive orientation.
Since $z$ has primitive $z^2/2$, $\oint_\gamma z\,dz=0$.
