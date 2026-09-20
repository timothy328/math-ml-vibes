---
name: generate-hw-problems
description: Generate a consolidated homework problem set for a math-ML topic, with multi-part questions that are solvable from the lecture and progress from easy to challenging.
---

# Generate Homework Problems

Use this skill to create or revise:
`subjects/<subject>/<topic>/hw/problems.md`.

## Required structure

Write exactly one consolidated Markdown file for the topic. Include:

- A clear title
- Five problems unless the user requests a different count
- Multiple subparts for every problem
- A progression from easy to medium
- One final challenge problem
- Questions that can be solved using the corresponding lecture and stated
  prerequisites

Do not split problems into separate files.

## Problem design

Use a balanced mix of:

- Definitions and conceptual checks
- Symbolic derivations
- Numerical or matrix calculations
- Interpretation and modeling questions
- At least one application connection where appropriate

Make every problem self-contained. Define all symbols, matrices, distributions,
domains, and initial conditions. State whether exact answers, explanations,
proofs, simulations, or pseudocode are expected.

Avoid requiring an unstated theorem, specialized software package, or topic
that appears only in the solution. The lecture may provide methods without
revealing the exact numerical answer.

## Math formatting

- Use `$...$` for inline mathematics.
- Use `$$...$$` for displayed equations.
- Prefer readable LaTeX such as `\frac`, `\sqrt`, `\nabla`, `\to`,
  `\leq`, `\mathbb{R}`, `\operatorname{diag}`, and matrix environments.
- Do not use backticks for ordinary mathematical expressions.
- Use backticks only for code, commands, paths, or literal identifiers.

## Quality checks

- Confirm that all five problems are represented in one file.
- Ensure difficulty increases and the final problem is the challenge problem.
- Ensure no answer key, solution steps, or hidden hints are included.
- Run `git diff --check` after editing.

