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

Populated topics use shortened descriptive names. The existing subjects have
12-topic roadmaps with Topic 1 populated; later topics currently contain only
empty `lecture`, `hw`, and `assessment` placeholders. New subjects may begin
as folder-only roadmaps before their lessons are developed.

## Subjects

- `real_analysis/`
  - `01_sequences_limits_continuity/` - Topic 1
- `discrete_math/`
  - `01_proofs_sets_relations_counting/` - Topic 1
- `diff_eq/`
  - `01_first_order_odes_linear_systems/` - Topic 1
- `optimization/`
  - `01_convexity_gradient_methods/` - Topic 1
  - `02_unconstrained_newton_methods/` - Topic 2
  - `03_constrained_optimization_kkt/` - Topic 3
  - `04_linear_programming/` - Topic 4
  - `05_quadratic_programming/` - Topic 5
  - `06_duality_sensitivity/` - Topic 6
  - `07_least_squares_regularization/` - Topic 7
  - `08_coordinate_proximal_methods/` - Topic 8
  - `09_stochastic_optimization/` - Topic 9
  - `10_dynamic_programming/` - Topic 10
  - `11_interior_point_methods/` - Topic 11 (graduate-level)
  - `12_advanced_variational_methods/` - Topic 12 (graduate-level)
- `bayesian_ml/`
  - `01_bayes_rule_conjugate_inference/` - Topic 1
- `complex_analysis/`
  - `01_complex_functions_contours/` - Topic 1
- `continuous_stochastic_processes/`
  - `01_brownian_motion_gaussian_processes/` - Topic 1
- `discrete_stochastic_processes/`
  - `01_markov_chains_stationarity/` - Topic 1
- `abstract_linear_algebra/`
  - `01_vectors_matrices_linear_systems/` - Topic 1
  - `02_vector_spaces_subspaces_bases/` - Topic 2
  - `03_linear_maps_change_of_basis/` - Topic 3
  - `04_inner_products_orthogonality/` - Topic 4
  - `05_least_squares_qr_factorization/` - Topic 5
  - `06_determinants_eigenvalues/` - Topic 6
  - `07_diagonalization_spectral_theory/` - Topic 7
  - `08_symmetric_matrices_svd/` - Topic 8
  - `09_positive_definite_matrices/` - Topic 9
  - `10_matrix_norms_conditioning/` - Topic 10
  - `11_linear_algebra_probability_statistics/` - Topic 11
  - `12_matrix_computations_applications/` - Topic 12

The stochastic-process subjects emphasize intuition, modeling, simulation,
and applications rather than proof-heavy treatment.

### Abstract Linear Algebra roadmap

The Abstract Linear Algebra sequence is an undergraduate bridge between
applied linear algebra and proof-oriented graduate mathematics or statistics.
It emphasizes precise definitions and reasoning while retaining computational
examples involving least squares, eigendecompositions, singular value
decompositions, positive-definite matrices, conditioning, and statistical
models. The final topics connect the theory to probability, statistics, and
reliable matrix computation without assuming a graduate algebra course.

## Claude generation skills

Reusable Claude skills for extending the curriculum live under
`.claude/skills/`:

- `generate-lecture/` - creates prerequisite-aware lecture notes
- `generate-hw-problems/` - creates one consolidated homework problem file
- `generate-hw-solutions/` - creates one consolidated worked-solution file
- `generate-assessment/` - creates a multi-part assessment without answers
- `generate-topic/` - creates a complete topic package from a subject

All four skills follow the repository's readable Markdown LaTeX convention.

### Optimization roadmap

The Optimization sequence contains 12 topics. Topics 1–10 are primarily
undergraduate material with direct connections to machine learning, numerical
methods, operations research, and control. Topics 11–12 are optional
graduate-level extensions.

## Python setup

Install [uv](https://docs.astral.sh/uv/) and create the project environment:

```bash
uv sync --dev
```

Run the starter tests:

```bash
uv run pytest
```
