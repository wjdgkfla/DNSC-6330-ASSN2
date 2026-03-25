# Assignment 2 - Explainability and Interpretability (COMPAS Replacement Model)

## Overview
This repository contains the Lecture 02 assignment implementation based on the cleaned COMPAS cohort.

Notebook included:
- `Compas_Analysis.ipynb`

The notebook includes:
1. Train/test split and model training.
2. Interpretable-by-design model: logistic regression.
3. Black-box model: gradient-boosted tree.
4. Group-level performance comparison by race.
5. Local explainability using LIME.
6. Global/local feature attribution using SHAP (beeswarm and waterfall).
7. Counterfactual recourse examples using DiCE.
8. Written responses for the mathematical and governance memo parts.

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `statsmodels`
- `scikit-learn`
- `lime`
- `shap`
- `dice-ml`

## Reproducibility Instructions
1. Create/activate a Python 3.11+ environment.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib statsmodels scikit-learn lime shap dice-ml
   ```
3. Open and run all cells in:
   - `Compas_Analysis.ipynb`

## Expected Outputs
- Race-wise model performance table (accuracy, FPR, FNR, AUC).
- LIME explanations for selected defendants.
- SHAP beeswarm and waterfall visualizations.
- DiCE counterfactual examples with immutable-feature checks.
- Governance interpretation text and memo section.

## AI Use Disclosure (Syllabus Requirement)
This submission includes disclosed GenAI-supported assistance consistent with GW AI guidance.

Tool used:
- OpenAI Codex (GPT-5)

Manner of contribution:
- Brainstorming and preparatory workflow structuring
- Exploratory support for coding/debugging explainability steps
- Documentation drafting support (README structure and wording)

Student integrity statement:
- All final code, analysis choices, and interpretations were critically reviewed and validated by the student.
- No restricted or regulated data was entered into third-party AI tools.

### Copy/Paste Disclosure Statement for Submission
"I used OpenAI Codex (GPT-5) for brainstorming, preparatory coding support, debugging assistance, and documentation drafting. I critically reviewed and validated all outputs, and the submitted work reflects my own final intellectual product. No restricted or regulated data was input into third-party AI systems."

## Notes
- Some explainability methods include randomness; results may vary slightly run-to-run unless seeds are fixed.
- Small metric differences across machines/libraries are normal.
