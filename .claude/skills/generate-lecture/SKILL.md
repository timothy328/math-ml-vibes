---
name: generate-lecture
description: Generate a collegiate-level math or ML lecture in Markdown with readable LaTeX, prerequisite-aware explanations, and practical data-science connections.
---

# Generate Lecture

Use this skill to create or revise a lecture file for a subject topic in
`subjects/<subject>/<topic>/lecture/lecture.md`.

## Required inputs

Before writing, identify:

- Subject and topic name
- Intended audience and prerequisites
- Whether the topic is undergraduate, graduate, proof-heavy, or
  application-focused
- Connections to data science, machine learning, numerical work, or modeling

Assume calculus, linear algebra, and statistics/probability unless the user
specifies otherwise.

## Required structure

Write one Markdown file with:

1. A title naming the subject and topic
2. A `## Learning goals` section
3. At least four ordered parts using headings such as
   `## Part 1 — ...`
4. Definitions, intuition, derivations, and worked setup
5. A practical workflow or summary section when appropriate

The lecture must teach the concepts needed to solve the corresponding
homework. Give methods and representative examples, but do not turn the
lecture into the exact homework answer key.

## Math formatting

- Use inline LaTeX with `$...$`.
- Use display LaTeX with `$$...$$` for multi-step or central equations.
- Prefer `\to`, `\leq`, `\geq`, `\nabla`, `\mathbb{R}`, `\mathbb{E}`,
  `\operatorname{Var}`, `\frac`, `\sum`, and `\begin{bmatrix}` over ASCII
  approximations.
- Do not place mathematical notation in backticks unless it is code,
  pseudocode, or a literal filename.
- Keep equations readable: use line breaks and aligned displays for long
  derivations.

## Quality checks

- Define symbols before using them.
- State domains, assumptions, and edge cases.
- Distinguish intuition from a theorem or guarantee.
- Keep stochastic-process topics non-proof-heavy when requested.
- Do not include unsupported claims or unexplained advanced notation.
- Run `git diff --check` after editing.

