# Fourier QNN Audit

Open-source tools for Fourier-based audits of trained quantum neural networks.

This repository is an early public scaffold for a toolkit that will help researchers test whether the frozen input-output behavior of trained quantum neural network (QNN) classifiers can be reproduced by compact Fourier surrogate models under transparent finite-sample validation protocols.

The goal is to make QNN model-behavior audits easier to reproduce, compare, and extend.

## Motivation

Quantum machine learning models are often evaluated through training accuracy, test accuracy, or architectural claims. These metrics are useful, but they do not fully answer a separate behavioral question:

> After training, what function did the QNN actually learn?

This project focuses on post-training audits of frozen QNN classifiers. In particular, it studies whether a trained QNN's predictions over a declared input distribution can be approximated or certified by a compact classical Fourier surrogate.

The toolkit is intended to support reproducible research, model auditing, and clearer benchmarking practices in quantum machine learning.

## Project status

This repository is currently a public scaffold.

The underlying research manuscript and paper-specific benchmark artifacts are being kept private while journal-submission constraints are resolved. Public releases will be added incrementally, with an emphasis on reusable software, documentation, and reproducible examples.

Planned public components include:

- Fourier surrogate fitting utilities
- finite-sample audit helpers
- candidate-selection and reporting workflows
- reproducible synthetic examples
- documentation for applying the protocol to trained QNN classifiers
- benchmark ledgers and reproducibility checks after journal constraints permit release

## Grant deliverable

A Unitary Foundation microgrant would support the first public release of this toolkit, including:

- a documented Python API for Fourier-based QNN audits
- finite-sample validation utilities
- small reproducible examples
- tutorial documentation
- a public roadmap for extending the toolkit to trained QNN classifiers
- guidance for preparing reproducible audit reports

The intended outcome is a usable open-source package that helps the quantum machine learning community evaluate trained QNN behavior more transparently.

## Repository layout

```text
fourier-qnn-audit/
├── docs/
│   ├── GRANT_SUMMARY.md
│   └── ROADMAP.md
├── examples/
│   └── README.md
├── src/
│   └── fourier_qnn_audit/
│       └── __init__.py
├── tests/
│   └── test_import.py
├── LICENSE
├── pyproject.toml
└── README.md
```

## Installation

This project is not yet released on PyPI.

For local development:

```bash
git clone https://github.com/bagheri365/fourier-qnn-audit.git
cd fourier-qnn-audit
python -m pip install -e .
```

Run the import test:

```bash
python -m pytest
```

## Planned API

The first public API is expected to support workflows such as:

```python
from fourier_qnn_audit import __version__

print(__version__)
```

Future versions will add utilities for:

```python
# planned interface sketch, not yet implemented

from fourier_qnn_audit import (
    fit_fourier_surrogate,
    validate_surrogate,
    AuditReport,
)

surrogate = fit_fourier_surrogate(
    qnn_outputs,
    inputs,
    max_terms=128,
)

report = validate_surrogate(
    qnn_outputs,
    surrogate_outputs,
    confidence=0.95,
)

print(report.summary())
```

## Roadmap

Near-term milestones:

1. Public package skeleton and installation instructions
2. Fourier surrogate interface
3. Finite-sample validation utilities
4. Small synthetic QNN-style examples
5. Tutorial notebook and documentation
6. Public audit-report format
7. Versioned release

Longer-term goals:

- support benchmark-style audit ledgers
- add reproducibility checks for published experiments
- support integration with common quantum ML workflows
- provide reviewer-friendly audit bundles for papers and preprints

## What is not public yet

To preserve journal-submission and review constraints, this public repository does not currently include:

- the full manuscript
- manuscript-specific LaTeX source
- paper-specific benchmark outputs
- full trained-model parameter files
- result tables tied to the submitted manuscript
- reviewer-response materials

These artifacts may be released later in an archival repository or reproducibility package, depending on journal policy and review constraints.

## Who this is for

This project is intended for:

- quantum machine learning researchers
- benchmark authors
- open-source quantum software developers
- researchers studying model auditability and reproducibility
- reviewers evaluating claims about trained QNN behavior

## License

This project is licensed under the MIT License.

## Citation

A citation will be added after the associated manuscript is publicly available.

For now, please cite the repository as:

```text
Bagheri, A. Fourier QNN Audit: Open-source tools for Fourier-based audits of trained quantum neural networks. GitHub repository, 2026.
```

## Contact

Maintainer: Alireza Bagheri

GitHub: [@bagheri365](https://github.com/bagheri365)