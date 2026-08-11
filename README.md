# Feature Selection using Soft Fuzzy Dominance Rough Sets (SFDRS)

An implementation of the Soft Fuzzy Dominance Rough Sets (SFDRS) algorithm for feature selection in monotonic classification problems, built to reproduce and validate results from the corresponding IEEE research paper.

## What it does

SFDRS is a rough-set-based feature selection method designed for **monotonic classification** tasks — problems where the class label increases (or stays the same) as the feature values increase (e.g., credit risk scoring, ordinal decision-making). It combines fuzzy dominance relations with rough set theory to identify a reduced, noise-robust feature subset without losing classification-relevant information.

This implementation reproduces the algorithm described in the IEEE paper *"Feature Selection with SFDRS for Monotonic Classification"* and validates it against the paper's reported results.

## How it works

1. **Fuzzy dominance relation** — Constructs a fuzzy relation over the dataset capturing degree of dominance between samples, rather than a strict crisp ordering.
2. **Rough approximation** — Computes lower/upper approximations of decision classes under the fuzzy dominance relation to identify which features are indispensable.
3. **Feature reduction** — Iteratively selects the minimal feature subset (reduct) that preserves the approximation quality of the full feature set.
4. **Noise robustness** — The "soft" fuzzy formulation is specifically designed to tolerate label/attribute noise better than crisp dominance-based rough set methods.

## Validation

Tested on the **Australian Credit Approval dataset** (a standard UCI benchmark for monotonic/ordinal classification), with results compared against the benchmarks reported in the source paper.

## Tech stack

`Python` · `Rough Set Theory` · `Fuzzy Logic` · `NumPy` / `Pandas`

## Files

- `Package.ipynb` — SFDRS algorithm implementation and evaluation
- `Paper Summary.pdf` — Summary of the source IEEE paper and its key results
- `australian - Copy.dat` — Australian Credit Approval dataset used for validation

## Notes

This was a research-reproduction project focused on implementing a published algorithm faithfully and validating it empirically, rather than proposing a novel method.
