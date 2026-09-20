---
name: generate-hw-solutions
description: Generate a consolidated worked solution file for a math-ML homework set, matching every problem and subpart without changing the problem statement.
---

# Generate Homework Solutions

Use this skill to create or revise:
`subjects/<subject>/<topic>/hw/solutions.md`.

Read the matching `hw/problems.md` and lecture before writing. Produce one
consolidated solution file; do not create one solution file per problem.

## Required structure

- A clear title
- One section for each homework problem, in the same order and with the same
  numbering as `problems.md`
- A response for every subpart
- Enough intermediate work to make reasoning checkable
- Final results clearly identified

Solutions should teach the method rather than only list answers. Include
assumptions, domain restrictions, units, normalization checks, or
interpretations whenever relevant.

## Correctness requirements

- Re-derive results instead of copying unsupported claims.
- Check algebra, signs, dimensions, boundary conditions, and probability
  normalization.
- For proofs, state the key implication or theorem being used.
- For algorithms or simulations, explain the state, update, and expected
  behavior.
- Keep the solution aligned with the lecture's notation.
- Do not add solutions to assessment files.

## Math formatting

- Use inline LaTeX with `$...$`.
- Use display LaTeX with `$$...$$` for substantial equations.
- Use readable forms such as `\frac`, `\sqrt`, `\nabla`, `\mathbb{E}`,
  `\operatorname{Var}`, `\begin{bmatrix}`, and `\begin{aligned}`.
- Avoid clunky ASCII math and avoid backticks around ordinary equations.
- Reserve backticks for code, commands, and literal identifiers.

## Quality checks

- Compare headings and numbering directly against `problems.md`.
- Confirm every subpart has a solution.
- Confirm no problem was silently altered.
- Run `git diff --check` after editing.

