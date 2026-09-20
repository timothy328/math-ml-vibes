# Real Analysis — Topic 1 Homework Solutions

## Problem 1

Given $\varepsilon>0$, choose
$N=\left\lceil\frac{3}{\varepsilon}\right\rceil+1$. For $n\geq N$,
$n>3/\varepsilon$, so
$$
\left|\frac{3}{n}-0\right|=\frac{3}{n}<\varepsilon.
$$
Therefore $3/n\to0$.

## Problem 2

1. Choose $N$ large enough that both $|a_n-a|<\varepsilon/2$ and
   $|b_n-b|<\varepsilon/2$; the triangle inequality gives the result.
2. For products, one sequence must be bounded; convergence supplies this
   boundedness.
3. Write $a_nb_n-ab=a_n(b_n-b)+b(a_n-a)$ and bound the two terms.

## Problem 3

$|(x^2+3x)-10|=|x-2||x+5|$. First require $|x-2|<1$, which gives
$|x+5|<8$. Choose $\delta=\min(1,\varepsilon/8)$. Then the product is less
than $\varepsilon$.

## Problem 4

1. $|x^2-a^2|=|x-a||x+a|$; restrict $|x-a|<1$ to bound $|x+a|$, then
   choose $\delta$ accordingly.
2. On $[0,1]$, $|x^2-y^2|=|x-y||x+y|\leq2|x-y|$, so the function is
   Lipschitz.
3. On all of $\mathbb{R}$, $|x+y|$ is not uniformly bounded, so this proof
   cannot use one global δ; in fact the function is not uniformly continuous.

## Problem 5

1. A continuous function on compact `[0,1]` is bounded.
2. The extreme value theorem gives points where the maximum and minimum are
   attained.
3. $|g(x)-g(y)|\leq K|x-y|\leq K\varepsilon$.
4. Input perturbations of at most $\varepsilon$ change the score by at most
   $K\varepsilon$.
