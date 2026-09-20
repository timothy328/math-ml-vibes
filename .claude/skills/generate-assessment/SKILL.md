---
name: generate-assessment
description: Generate an answer-free assessment for a math-ML topic with multi-part problems that test understanding beyond routine homework.
---

# Generate Assessment

Use this skill to create or revise:
`subjects/<subject>/<topic>/assessment/assessment.md`.

Read the matching lecture and homework files before writing. The assessment
must be answer-free.

## Required structure

- A clear subject and topic title
- An explicit statement that no solutions are provided
- Four problems unless the user requests a different count
- More subparts per problem than the corresponding homework
- A mixture of conceptual, derivational, computational, and interpretive
  questions
- At least one problem that requires synthesis or transfer to a new setting

Questions should be solvable from the lecture and prerequisites but should not
copy the homework numbers or wording. Increase the reasoning burden through
case analysis, justification, interpretation, or comparison rather than by
introducing unexplained advanced material.

## Strict answer boundary

Do not include:

- Numerical answers
- Proof outlines that reveal the main argument
- Worked equations leading to the result
- Hints labeled as hints
- A solution section, answer section, or answer key

It is acceptable to state definitions, givens, constraints, and what the
student must show.

## Math formatting

- Use `$...$` for inline mathematics.
- Use `$$...$$` for displayed mathematics.
- Prefer `\to`, `\leq`, `\geq`, `\nabla`, `\mathbb{R}`, `\frac`,
  `\operatorname{Var}`, and matrix environments over ASCII notation.
- Do not wrap ordinary equations in backticks.
- Keep long expressions in display blocks for readability.

## Quality checks

- Confirm exactly four top-level problems by default.
- Confirm each problem has more subparts than a typical homework problem.
- Search the finished file for terms such as `solution`, `answer`, and `therefore`
  and remove accidental answer content while preserving the no-solutions
  notice.
- Run `git diff --check` after editing.
