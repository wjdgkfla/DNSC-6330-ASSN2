# Assignment 2 - Explainability and Interpretability (COMPAS Replacement Model)

## Purpose of the Analysis
This repository reproduces the Lecture 02 COMPAS explainability workflow in Python. The goal is to preserve all substantive analytical steps: model building, group-level diagnostics, explainability analysis, counterfactual recourse, and interpretation.
Assignment 2 is implemented as a continuation of Assignment 1, using the same cleaned COMPAS cohort and aligned variable definitions.
The Assignment 2 section is written in a student-friendly style and directly follows the four Individual Homework 2 tasks from Lecture 02.

Notebook included:
- `Assignment 2.ipynb`

Reference materials used:
- `DNSC_6330_Lecture-02.pdf`
- Lecture 01 cleaned COMPAS workflow as the baseline pipeline

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `statsmodels`
- `scikit-learn`
- `lime`
- `shap`
- `dice-ml`

## How This Notebook Matches the Assignment Rubric
### 1) Build and Compare Models
- Uses cleaned COMPAS features and target with train/test split.
- Trains logistic regression as the interpretable-by-design baseline.
- Trains gradient-boosted tree as the black-box comparison model.

### 2) Evaluate Group-Level Performance and Diagnostics
- Computes race-level performance metrics.
- Reports accuracy, FPR, FNR, and AUC by group.
- Reproduces fairness-focused diagnostic comparisons across racial groups.

### 3) Generate Explainability Outputs
- Produces SHAP explanations (global beeswarm + local waterfall).
- Produces LIME local explanations for selected defendants.
- Compares SHAP and LIME attribution patterns in plain language (agreement, divergence, governance implication).

### 4) Generate Counterfactual Recourse and Interpretation
- Uses DiCE to generate counterfactuals for selected individuals.
- Checks whether immutable features are required to flip predictions.
- Includes written interpretation and governance-oriented discussion.

### 5) Documentation and Reproducibility
- Notebook is organized from data preparation to interpretability outputs.
- Major workflow stages are labeled and explained.
- Running cells top-to-bottom reproduces the analysis outputs.

## Reproducibility Instructions
1. Create and activate a Python 3.11+ environment.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib statsmodels scikit-learn lime shap dice-ml
   ```
3. Open Jupyter and run all cells in:
   - `Assignment 2.ipynb`

## Expected Outputs
- Race-wise model performance table (accuracy, FPR, FNR, AUC).
- SHAP beeswarm and waterfall plots.
- LIME explanations for selected defendants.
- DiCE counterfactual tables with immutable-feature checks.
- Written interpretation and governance memo content.

## How to Use This Notebook
- Read sections in order from model setup to interpretation.
- Run cells top-to-bottom to reproduce all outputs.
- Use the Expected Outputs section to verify your run completed successfully.

## Note on Minor Differences
Small run-to-run differences can occur in explainability outputs due to stochastic components (for example, perturbation/sampling in LIME/SHAP/DiCE). Substantive conclusions remain consistent.
