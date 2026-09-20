# Discrete Math — Topic 1 Homework Solutions

## Problem 1

1. `∀n ∈ Z, n odd => n^2 odd`.
2. If `n=2k+1`, then `n^2=4k^2+4k+1=2(2k^2+2k)+1`, which is odd.
3. The contrapositive is “if `n^2` is even, then `n` is even.” It is
   equivalent because a conditional and its contrapositive always share a
   truth value.

## Problem 2

1. For any `x`, `x` is not in `A ∩ B` exactly when `x` is not in `A` or
   `x` is not in `B`; therefore `(A ∩ B)^c=A^c∪B^c`.
2. `x ∈ A-(B∪C)` means `x∈A`, `x∉B`, and `x∉C`, which is exactly
   `x∈(A-B)∩(A-C)`.
3. These identities describe equivalent ways to combine filters and negate
   filter membership.

## Problem 3

1. `binom(8,3)=56`.
2. `56*4=224`.
3. `8*7*6*4=1,344`.
4. A subset ignores order, while an ordered selection distinguishes all
   permutations.

## Problem 4

1. Reflexivity follows because `a-a=0` is divisible by 3. Symmetry follows
   because if 3 divides `a-b`, it divides `b-a`. Transitivity follows because
   sums of multiples of 3 are multiples of 3.
2. The classes are integers congruent to 0, 1, or 2 modulo 3.
3. `-10` is congruent to 2 modulo 3, so it is in the class of 2.
4. Each class contains precisely the integers with the same remainder on
   division by 3.

## Problem 5

1. The degree sum is `8*3+4*2=32`, so the graph has `32/2=16` edges.
2. The degree sum is even, satisfying the handshaking lemma; this establishes
   compatibility with the necessary condition.
3. Inclusion-exclusion gives `40+30-12=58`.
4. Exactly one rule gives `(40-12)+(30-12)=46`, so the estimate is `0.46`.

