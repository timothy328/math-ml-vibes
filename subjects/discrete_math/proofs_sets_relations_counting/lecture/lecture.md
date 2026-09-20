# Discrete Math — Topic 1: Proofs, Sets, Relations, and Counting

## Learning goals

By the end of this topic, you should be able to translate informal claims
into precise statements, choose an appropriate proof strategy, reason about
sets and relations, and apply basic counting principles to data-science
problems.

## Part 1 — Mathematical language and proof structure

### Statements and quantifiers

A proposition is a statement that is either true or false. Common
quantifiers are:

- `∀ x ∈ S`: for every `x` in `S`
- `∃ x ∈ S`: there exists an `x` in `S`
- `∃! x ∈ S`: there exists exactly one `x` in `S`

Negate quantifiers by switching them and negating the predicate:

`¬(∀x, P(x))` is equivalent to `∃x such that ¬P(x)`.

### Proof strategies

- **Direct proof:** assume the hypotheses and derive the conclusion.
- **Contrapositive:** prove `not conclusion => not hypothesis`.
- **Contradiction:** assume the claim is false and derive an impossibility.
- **Cases:** partition the domain into exhaustive, non-overlapping cases.
- **Induction:** prove a base case, then prove the inductive implication.
- **Counterexample:** disprove a universal claim with one valid exception.

For an industry ML connection, a metric claim such as “every training loss
decreases after an update” is universal; one reproducible counterexample is
enough to reject it.

## Part 2 — Sets, functions, and relations

For sets `A` and `B`, union, intersection, difference, and complement are
defined elementwise. The power set `P(A)` is the set of all subsets of `A`;
if `|A| = n`, then `|P(A)| = 2^n`.

A function `f: A -> B` assigns exactly one output in `B` to every input in
`A`. It is injective if equal outputs imply equal inputs, and surjective if
every element of `B` is achieved.

A relation `R` on `A` is:

- reflexive if `aRa` for every `a`
- symmetric if `aRb => bRa`
- transitive if `aRb` and `bRc => aRc`

An equivalence relation is reflexive, symmetric, and transitive. It partitions
the domain into equivalence classes.

## Part 3 — Counting and recurrences

The addition rule handles disjoint alternatives; the multiplication rule
handles sequential choices. For `n` distinct objects:

- ordered selections of `k`: `n!/(n-k)!`
- unordered selections of `k`: `binom(n,k)`
- subsets of any size: `2^n`

Use inclusion-exclusion for overlapping events:

`|A ∪ B| = |A| + |B| - |A ∩ B|`.

A recurrence defines a quantity from smaller instances. A standard proof of a
closed form uses induction. In algorithm analysis, recurrence structure often
reveals whether a method is linear, logarithmic, or exponential.

## Part 4 — Graphs and discrete probability

A graph `G=(V,E)` models entities and relationships. Degree counts incident
edges. A path is a sequence of adjacent vertices; a connected graph has a
path between every pair of vertices.

For a finite sample space, probability is a normalized count. Conditional
probability is:

`P(A | B) = P(A ∩ B) / P(B)`, when `P(B) > 0`.

Independence means `P(A ∩ B)=P(A)P(B)`, not merely that the events look
unrelated. This distinction matters when evaluating data leakage and feature
relationships.

