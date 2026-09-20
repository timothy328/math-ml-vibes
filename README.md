# math-ml-vibes

A structured self-study workspace for collegiate mathematics and
mathematically grounded machine learning, designed for someone with several
years of data-science industry experience.

## Learning structure

Each subject is organized as:

```text
subject/
└── topic_1/
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

The first topic in each subject is intentionally a placeholder for the first
lesson to be designed.

## Subjects

- `real_analysis/`
- `discrete_math/`
- `diff_eq/`
- `optimization/`
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
