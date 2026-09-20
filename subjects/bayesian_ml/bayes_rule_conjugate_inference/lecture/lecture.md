# Topic 1: Bayes Rule and Conjugate Inference

## Learning goals

This topic develops the basic Bayesian workflow: state a generative model,
combine prior and likelihood with Bayes' rule, recognize conjugate families,
make posterior and predictive calculations, and choose actions under a loss
function. The emphasis is on keeping random quantities, observed data, and
decisions distinct.

## Part 1 — Bayes' rule as an update

For a parameter $\theta$, data $D$, and hypothesis or event $H$,
$$
p(\theta\mid D)=\frac{p(D\mid\theta)p(\theta)}{p(D)}\propto
p(D\mid\theta)p(\theta).
$$
The prior $p(\theta)$ represents uncertainty before observing $D$, the
likelihood $p(D\mid\theta)$ describes the data model, and the evidence
$$
p(D)=\int p(D\mid\theta)p(\theta)\,d\theta
$$
normalizes the posterior. For discrete hypotheses,
$P(H_i\mid D)\propto P(D\mid H_i)P(H_i)$ and the denominator is a sum.

For iid data $D=(x_1,\ldots,x_n)$, the likelihood is
$p(D\mid\theta)=\prod_i p(x_i\mid\theta)$. Log likelihoods turn products into
sums; terms independent of $\theta$ can be dropped when deriving a posterior
up to proportionality. A useful diagnostic is that posterior log density is
log likelihood plus log prior.

## Part 2 — Beta-Bernoulli and Dirichlet-categorical models

If $x_i\in\{0,1\}$ and $x_i\mid\theta\sim\operatorname{Bernoulli}(\theta)$,
choose $\theta\sim\operatorname{Beta}(\alpha,\beta)$, whose density is
proportional to $\theta^{\alpha-1}(1-\theta)^{\beta-1}$. With $s$ successes
and $f$ failures,
$$
\theta\mid D\sim\operatorname{Beta}(\alpha+s,\beta+f).
$$
The posterior mean is $(\alpha+s)/(\alpha+\beta+n)$ and the mode (when both
shape parameters exceed one) is $(\alpha+s-1)/(\alpha+\beta+n-2)$.

For $K$ categories, $\boldsymbol{\theta}\sim
\operatorname{Dirichlet}(\boldsymbol{\alpha})$ and categorical counts
$\mathbf{n}$ give
$$
\boldsymbol{\theta}\mid D\sim
\operatorname{Dirichlet}(\boldsymbol{\alpha}+\mathbf{n}).
$$
The posterior predictive probability of category $k$ is
$(\alpha_k+n_k)/(\alpha_0+n)$ where $\alpha_0=\sum_k\alpha_k$.

## Part 3 — Gaussian conjugacy and posterior prediction

Suppose observations satisfy $x_i\mid\mu\sim\mathcal N(\mu,\sigma^2)$ with
known $\sigma^2$, and prior $\mu\sim\mathcal N(\mu_0,\tau_0^2)$. The posterior
is normal with precision (inverse variance) addition:
$$
\frac{1}{\tau_n^2}=\frac{1}{\tau_0^2}+\frac{n}{\sigma^2},\qquad
\mu_n=\tau_n^2\left(\frac{\mu_0}{\tau_0^2}
+\frac{n\bar x}{\sigma^2}\right).
$$
Thus data and prior means are precision-weighted. For a new observation,
integrating out $\mu$ gives
$$
x_{\mathrm{new}}\mid D\sim\mathcal N(\mu_n,\sigma^2+\tau_n^2).
$$
The extra $\tau_n^2$ is parameter uncertainty; plugging in $\mu_n$ would
understate predictive variation.

## Part 4 — Decisions, intervals, and model checking

Bayesian inference is not complete until an action is selected. Under squared
error loss $L(a,\theta)=(a-\theta)^2$, the posterior mean minimizes posterior
expected loss. Under absolute error, the posterior median is optimal; under
0–1 loss for a discrete parameter, a posterior mode is optimal. For a finite
action set, compute posterior risk
$$
\rho(a\mid D)=\mathbb E[L(a,\theta)\mid D]
$$
and choose the action with smallest risk.

A credible interval $[l,u]$ satisfies
$P(l\le\theta\le u\mid D)=1-\gamma$. It is a probability statement about
$\theta$ under the posterior, not a repeated-sampling claim about a fixed
parameter. Posterior predictive checks simulate replicated data from
$p(\tilde D\mid D)=\int p(\tilde D\mid\theta)p(\theta\mid D)d\theta$ and
compare summaries, such as a mean or maximum, with the observed data.

## Part 5 — A reusable workflow

1. Identify the quantity of interest and the sampling model.
2. State a prior and its assumptions; record known versus unknown variance.
3. Write likelihood and prior in a common kernel, then normalize or identify a
   conjugate family.
4. Compute posterior summaries and, when predicting, integrate parameter
   uncertainty rather than simply plugging in a point estimate.
5. Match the summary or decision to the loss, and check sensitivity to the
   prior and to model mismatch.

