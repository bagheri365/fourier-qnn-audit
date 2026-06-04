# Fourier QNN Audit Toolkit

Open-source toolkit for auditing trained quantum neural networks (QNNs) with compact Fourier surrogate models and finite-sample validation protocols.

> Status: early public project scaffold. Full paper-specific benchmark artifacts will be released after journal-submission constraints are resolved.

## Motivation

Quantum neural networks are often evaluated by task accuracy. This project focuses on a complementary question: after a QNN is trained and frozen, how complex is its input-output behavior under a declared audit distribution?

The toolkit will provide reproducible utilities for:

- fitting compact Fourier surrogate models to frozen QNN outputs;
- evaluating finite-sample audit certificates;
- separating QNN-behavior audits from label-trained classical baselines;
- producing transparent benchmark ledgers and documentation.

## Planned deliverables

The first public release will include:

1. A small Python package for Fourier surrogate fitting and audit evaluation.
2. Minimal examples on synthetic and toy QNN-style functions.
3. Documentation explaining the audit protocol and interpretation guardrails.
4. Reproducibility scripts for public, non-paper-specific examples.

## What is not included yet

The full manuscript, exact paper result tables, and complete benchmark evidence bundle are intentionally not included in this initial public scaffold while journal submission and review constraints are being handled.

## License

MIT License. See `LICENSE`.
