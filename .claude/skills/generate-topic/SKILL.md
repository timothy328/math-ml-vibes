---
name: generate-topic
description: Generate a complete subject topic package with a lecture, consolidated homework problems, worked homework solutions, and an answer-free assessment.
---

# Generate Topic

Use this skill when the user provides a subject and asks for the next topic,
a first topic, or a complete lesson package.

## Required input

Identify:

- Subject name
- Topic number or sequence position
- Whether the topic is undergraduate, graduate, proof-heavy, or
  application-focused
- Intended prerequisites
- Desired connection to data science, machine learning, numerical methods,
  modeling, or another application area

Assume calculus, linear algebra, and statistics/probability unless the user
specifies different prerequisites.

## Topic naming and location

Create a concise, descriptive, filesystem-safe topic directory:

```text
subjects/<subject>/<topic_name>/
```

Use a shortened snake_case name based on the actual topic, not a generic
`topic_1`, when the topic content has been written. Preserve existing
directories and materials. Do not overwrite a populated topic without
explicit permission.

## Required files

Create exactly this content structure:

```text
<topic_name>/
├── lecture/
│   └── lecture.md
├── hw/
│   ├── problems.md
│   └── solutions.md
└── assessment/
    └── assessment.md
```

Do not split homework problems or solutions into separate files.

## Lecture requirements

The lecture must:

- Use a clear subject/topic title.
- Include learning goals.
- Contain at least four ordered parts.
- Define notation before using it.
- Explain concepts, intuition, methods, assumptions, and edge cases.
- Provide enough context to solve the homework without revealing its exact
  answers.
- Include practical or ML/data-science connections when appropriate.
- Keep stochastic-process topics intuition- and application-focused rather
  than proof-heavy when requested.

Longer lectures are appropriate for advanced or foundational subjects.

## Homework requirements

Create exactly one `hw/problems.md` with five multi-part problems by default:

- Problems 1–2: easy
- Problems 3–4: medium
- Problem 5: challenge

Questions must be solvable from the lecture and stated prerequisites. Include
a mix of conceptual, symbolic, numerical, computational, proof, and
interpretive work as appropriate to the subject. Define every matrix,
distribution, domain, initial condition, and convention used.

Create exactly one `hw/solutions.md` containing worked solutions for every
problem and subpart. Match the numbering and notation in `problems.md`.
Show enough intermediate reasoning to make the method checkable.

## Assessment requirements

Create exactly one `assessment/assessment.md` with four top-level problems by
default. Each problem should have more subparts than the homework problems
and should test transfer, synthesis, justification, or interpretation.

The assessment must contain no answers. Do not include:

- Numerical results
- Proof outlines
- Worked derivations
- Hidden hints
- Solution or answer-key sections

Include an explicit statement that no solutions are provided.

## Math formatting

Use the repository's readable Markdown LaTeX convention everywhere:

- Inline math: `$...$`
- Display math: `$$...$$`
- Prefer `\to`, `\leq`, `\geq`, `\nabla`, `\mathbb{R}`, `\mathbb{E}`,
  `\operatorname{Var}`, `\frac`, `\sum`, and matrix environments.
- Use `\begin{aligned}` or line breaks for long derivations.
- Do not wrap ordinary mathematical expressions in backticks.
- Reserve backticks for code, commands, paths, and literal identifiers.

## README and roadmap updates

Update the root `README.md` when a new subject topic is added:

- Add the descriptive topic directory under the subject.
- Preserve the attribution section and existing topic listings.
- If the subject has a defined sequence, keep topic numbering clear.

## Validation checklist

Before finishing:

1. Confirm all five required files exist.
2. Confirm the lecture has at least four parts.
3. Confirm `problems.md` has five top-level problems.
4. Confirm `solutions.md` covers all five problems.
5. Confirm `assessment.md` has four top-level problems and no answers.
6. Search the assessment for accidental solution language.
7. Run `git diff --check`.
8. Run the existing project tests when code or project metadata changed.

