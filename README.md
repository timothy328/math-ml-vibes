# math-ml-vibes

A structured self-study workspace for collegiate mathematics and
mathematically grounded machine learning, designed for someone with several
years of data-science industry experience.

## Attribution

This study workspace was built using GPT 5.6 Luna.

## Learning structure

Each subject is organized as:

```text
subject/
└── topic_name/
    ├── lecture/
    ├── hw/
    │   ├── problems.md
    │   └── solutions.md
    └── assessment/
```

- `lecture/` - notes, worked examples, and references
- `hw/problems.md` - all homework questions
- `hw/solutions.md` - all homework solutions
- `assessment/` - quizzes, exams, and self-checks

Populated topics use shortened descriptive names. Subjects without written
materials yet retain the `topic_1/` placeholder.

## Subjects

- `real_analysis/`
  - `sequences_limits_continuity/` - Topic 1
- `discrete_math/`
  - `proofs_sets_relations_counting/` - Topic 1
- `diff_eq/`
- `optimization/`
  - `convexity_gradient_methods/` - Topic 1
- `bayesian_ml/`
- `complex_analysis/`
- `continuous_stochastic_processes/`
- `discrete_stochastic_processes/`

The stochastic-process subjects emphasize intuition, modeling, simulation,
and applications rather than proof-heavy treatment.

## Python setup

Install [uv](https://docs.astral.sh/uv/) and create the project environment:

```bash
uv sync --dev
```

Run the starter tests:

```bash
uv run pytest
```
