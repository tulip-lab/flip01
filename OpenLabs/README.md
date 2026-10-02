# Pattern Classification Open Labs

This directory turns selected `flip01` notebooks into a coherent seven-lab
Pattern Classification sequence. The original notebooks remain in the
repository root as source material; the Open Labs are self-contained,
offline-first, and use current scikit-learn APIs.

Each lab is designed for an approximately two-hour session and follows the
same structure:

1. Overview
2. Learning Objectives
3. Prerequisites
4. Session Plan
5. Background Concepts
6. Setup
7. Guided Practice
8. Student Challenge
9. Testing and Debugging
10. Extension Task
11. Submission and Reflection
12. References

## Lab map

| Open Lab | Course module | Source notebook(s) | Observable learning outcomes | Status |
|---|---|---|---|---|
| [PC01](PC01-Classification-Workflow-and-Features.ipynb) | Module 1 — Classification Workflow & Features | `F1B-00-MLPipeline`, `F1B-03-MLPolyFeaGeneration`, `F1B-04-MLSampleGenerators` | Build a leakage-safe pipeline; reason about generated and interaction features; compare with a baseline | Ready |
| [PC02](PC02-Bayesian-Decision-and-Boundaries.ipynb) | Module 2 — Bayesian Decision & Decision Boundaries | `F1A-01-DecisionBoundaries` | Compute Gaussian discriminants; plot boundaries; explain prior and introductory cost effects | Ready |
| [PC03](PC03-Parameter-Estimation-MLE-MAP-EM.ipynb) | Module 3 — Parameter Estimation: MLE, MAP & EM | `F1A-02-EM`, selected concepts from `F1A-00-Bayesian` | Contrast MLE and MAP; fit and diagnose a Gaussian mixture; evaluate EM initialisation | Ready |
| [PC04](PC04-Probabilistic-Models-HMM-and-Naive-Bayes.ipynb) | Module 4 — Probabilistic Models: HMM + Naive Bayes | `F1A-03-HMM`; new Naive Bayes bridge material | Evaluate Gaussian Naive Bayes; decode an HMM in log space; validate probability tables | Ready |
| [PC05](PC05-Non-parametric-Classification-Parzen-and-KNN.ipynb) | Module 5 — Non-parametric Classification: Parzen + KNN | `F1A-04-ParzenWindow`, `F1A-05-KNN` | Build class-conditional KDE and KNN classifiers; connect smoothing to bias and variance | Ready |
| [PC06](PC06-Discriminant-Functions-Optimisation-and-SVM.ipynb) | Module 6 — Discriminant Functions, Optimisation & SVM | `F1A-06`, `F1A-07`, `F1A-08`, `F1A-09-SVM` | Optimise a discriminant; inspect convergence; compare linear and kernel margins | Ready |
| [PC07](PC07-Model-Selection-and-Generalisation.ipynb) | Module 7 — Model Selection & Generalisation | `F1B-00-MLPipeline`, `F1B-01-MLGridSearch`, `F1B-02-MLValidationCurves` | Separate selection from assessment; tune a pipeline; interpret validation and learning curves | Ready |

“Ready” means the guided path runs from a fresh kernel with the dependencies
below. Student challenge cells are deliberately incomplete but execute safely;
students supply the analysis described by the success criteria.

## Running the labs

Use Python 3.10 or newer. From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
python -m pip install -r OpenLabs/requirements.txt
jupyter lab OpenLabs
```

The labs use generated data or datasets bundled with scikit-learn. They do not
depend on the current working directory, repository data paths, or network
access. Fixed random seeds make the guided results reproducible.

## Teaching and submission notes

- Guided practice provides the minimum worked pathway; it is not a model
  answer to the student challenge.
- Each challenge has observable success criteria and reserves the held-out
  test set until after model selection.
- Testing cells check invariants and common implementation errors. Passing a
  check does not replace interpretation.
- Students should submit executed output, a compact result or figure, and a
  150–250 word evidence-based reflection.
- Collaboration and external or AI assistance should be acknowledged. Local
  policy wording can be added by the teaching team; none is invented here.

## Material still to add

The following topics are not yet supported by a complete source notebook and
should be developed as dedicated follow-on labs or substantial extensions:

| Proposed lab/module | Current gap | Suggested evidence-producing activity |
|---|---|---|
| Bayesian risk and cost-sensitive classification (deeper treatment) | PC02 introduces a binary threshold but does not cover general loss matrices, reject options, calibration, or empirical decision-curve analysis | Compare calibrated posteriors under multiple loss matrices and plot expected risk across operating conditions |
| Bayesian Networks | No focused source notebook | Specify a small DAG, compute conditional independencies, learn parameters, and perform exact/approximate inference |
| LDA and feature extraction | Decision boundaries exist, but there is no systematic feature-extraction lab | Derive Fisher's criterion, project high-dimensional data, and compare with PCA without leaking labels |
| PAC learning and generalisation theory | No source material | Estimate empirical sample complexity, explore hypothesis-class capacity, and relate observed gaps to theoretical bounds |
| Modern deep pattern classification | Current repository predates a modern deep-learning workflow | Train a small neural classifier with a CPU-friendly dataset, learning curves, calibration, ablation, and reproducibility controls |

Additional useful material would cover Bayesian-network structure learning,
multiclass cost matrices, probability calibration, dataset shift, fairness
diagnostics, and a capstone that connects all seven modules.

## Provenance and maintenance

The source mapping above is part of each notebook's metadata under `openlab`.
When updating a lab, keep its learning objectives, challenge evidence, tests,
and references aligned. Prefer stable public APIs from NumPy, Matplotlib,
SciPy, and scikit-learn; avoid network downloads and machine-specific paths.
