# Real Analysis — Topic 1 Homework Solutions

## Problem 1

Given `ε>0`, choose `N=ceil(3/ε)+1`. For `n≥N`, `n>3/ε`, so
`|3/n-0|=3/n<ε`. Therefore `3/n -> 0`.

## Problem 2

1. Choose `N` large enough that both `|a_n-a|<ε/2` and
   `|b_n-b|<ε/2`; the triangle inequality gives the result.
2. For products, one sequence must be bounded; convergence supplies this
   boundedness.
3. Write `a_nb_n-ab=a_n(b_n-b)+b(a_n-a)` and bound the two terms.

## Problem 3

`|(x^2+3x)-10|=|x-2||x+5|`. First require `|x-2|<1`, which gives
`|x+5|<8`. Choose `δ=min(1,ε/8)`. Then the product is less than `ε`.

## Problem 4

1. `|x^2-a^2|=|x-a||x+a|`; restrict `|x-a|<1` to bound `|x+a|`, then
   choose δ accordingly.
2. On `[0,1]`, `|x^2-y^2|=|x-y||x+y|≤2|x-y|`, so the function is Lipschitz.
3. On all of `R`, `|x+y|` is not uniformly bounded, so this Lipschitz proof
   cannot use one global δ; in fact the function is not uniformly continuous.

## Problem 5

1. A continuous function on compact `[0,1]` is bounded.
2. The extreme value theorem gives points where the maximum and minimum are
   attained.
3. `|g(x)-g(y)|≤K|x-y|≤Kε`.
4. Input perturbations of at most ε change the score by at most `Kε`.

