# Discrete Math — Topic 1 Homework

## Problem 1 — Proof translation (Easy)

Let $P(n)$ be the statement “if $n$ is odd, then $n^2$ is odd,” for an
integer $n$.

1. Write the statement using quantifiers.
2. Prove it directly.
3. Write its contrapositive and explain why it is equivalent.

## Problem 2 — Set identities (Easy)

Let `A`, `B`, and `C` be subsets of a universal set `U`.

1. Prove $(A \cap B)^c = A^c \cup B^c$.
2. Prove $A \setminus (B \cup C) = (A\setminus B) \cap (A\setminus C)$.
3. Give a plain-language interpretation of each identity using dataset
   filters.

## Problem 3 — Counting (Medium)

A data pipeline has 8 candidate features. It must select 3 features and then
choose one of 4 model families.

1. How many feature subsets are possible?
2. How many feature-subset/model-family configurations are possible?
3. If feature order matters for a downstream ordered transform, how many
   configurations are possible when selecting 3 distinct features?
4. Explain why the answers to parts 1 and 3 differ.

## Problem 4 — Relations and equivalence classes (Medium)

Define a relation on integers by $a \sim b$ if and only if $a-b$ is divisible
by 3.

1. Prove that `~` is an equivalence relation.
2. Describe all equivalence classes.
3. Which class contains `-10`?
4. Explain how these classes relate to taking an integer modulo 3.

## Problem 5 — Graphs and inclusion-exclusion (Challenge)

An undirected graph has 12 vertices. Eight vertices have degree 3, and four
vertices have degree 2.

1. Determine the number of edges.
2. Explain why the degree sequence is compatible with an undirected graph.
3. In a separate experiment, 40 records satisfy rule `A`, 30 satisfy rule
   `B`, and 12 satisfy both. How many satisfy at least one rule?
4. If 100 records are sampled uniformly, estimate the probability that a
   record satisfies exactly one of the two rules.
