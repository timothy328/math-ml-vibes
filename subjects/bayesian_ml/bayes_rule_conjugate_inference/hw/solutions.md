# Homework Solutions: Bayes Rule and Conjugate Inference

## Problem 1

The positive-test probability is
$0.95(0.02)+0.08(0.98)=0.0974$. Hence
$$
P(H\mid+)=\frac{0.95(0.02)}{0.0974}\approx0.1951.
$$
For a negative result, $P(-\mid H)=0.05$ and $P(-\mid H^c)=0.92$, so
$$
P(H\mid-)=\frac{0.05(0.02)}{0.05(0.02)+0.92(0.98)}
\approx0.00111.
$$
The $95\%$ is $P(+\mid H)$, not the reverse conditional probability; the
base rate and false positives determine the reverse probability.

## Problem 2

The posterior is $\operatorname{Beta}(2+7,3+3)=\operatorname{Beta}(9,6)$.
Its mean is $9/15=0.6$ and its mode is $(9-1)/(15-2)=8/13$.
The probability of two future successes is
$$
\mathbb E[\theta^2\mid D]
=\frac{9\cdot10}{15\cdot16}=\frac{3}{8}.
$$
The prior mean was $2/5=0.4$; seven successes move the mean to $0.6$ while
the increased total shape makes the posterior more concentrated.

## Problem 3

The posterior is $\operatorname{Dirichlet}(9,7,8)$. Category 2 has predictive
probability $7/(9+7+8)=7/24$. The posterior expected vector is
$(9/24,7/24,8/24)$. The concentration is $24$: larger concentration means
less posterior variance and therefore more certainty in the category
probabilities, while the predictive mean remains the normalized parameter
vector.

## Problem 4

Prior precision is $1/9$ and data precision is $9/4$, so
$$
\tau_n^2=\frac{1}{1/9+9/4}=\frac{36}{85}.
$$
The posterior mean is
$$
\mu_n=\frac{(1/9)10+(9/4)12}{1/9+9/4}
$$
Since $(10/9+27)=253/9$ and $1/9+9/4=85/36$, this is
$\mu_n=(253/9)(36/85)=1012/85\approx11.906$.
Thus $\mu\mid D\sim\mathcal N(1012/85,36/85)$. A new observation has
$$
x_{\rm new}\mid D\sim\mathcal N(1012/85,\;4+36/85).
$$
The squared-error Bayes action is $1012/85$. The posterior variance
$36/85\approx0.424$ is much smaller than the prior variance $9$.

## Problem 5

The posterior risk of intervention is
$$
\rho(1\mid D)=4(1-q)+1q=4-3q,
$$
while no intervention has risk $\rho(0\mid D)=3q$. Choose $a=1$ when
$4-3q<3q$, namely $q>2/3$; either action ties at $q=2/3$. Thus $q=0.3$
selects $a=0$, and $q=0.8$ selects $a=1$. Increasing the false-positive loss
$L(1,0)$ makes intervention less attractive and raises the threshold.
