# Liver Disease Prediction

Predict whether a patient has liver disease using routine clinical lab values.

## Problem Overview
- **Goal**: Binary classification—predict liver disease vs. no liver disease.
- **Why it matters**: Early detection can reduce clinician workload and improve patient outcomes.

## Dataset
- 583 records collected in North East Andhra Pradesh, India.
  - 416 liver disease cases, 167 non-liver cases.
  - 441 male, 142 female patients.
- Ages over 89 are recorded as 90.
- Source columns include a `Dataset` label indicating liver disease (1) or not (2).

## Features
- Age, Gender
- Total Bilirubin, Direct Bilirubin
- Alkaline Phosphotase
- Alamine Aminotransferase
- Aspartate Aminotransferase
- Total Proteins
- Albumin
- Albumin/Globulin Ratio

## ML Framing
- **Type**: Supervised binary classification.
- **Target**: `Dataset` (1 = liver disease, 2 = no disease).
- **Typical models**: Logistic Regression, Random Forest, Gradient Boosting, etc.

## Evaluation
- **ROC-AUC**: Primary metric to compare models by their ranking quality.
- **Confusion matrix / sensitivity / specificity**: To understand error types and class balance handling.

## Suggested Workflow
1) EDA: Check missing values, class balance, and feature distributions.
2) Preprocess: Handle missingness, encode gender, scale numeric features if needed.
3) Modeling: Train baseline, then tune tree-based / ensemble methods.
4) Validation: Use stratified splits and cross-validation; watch for class imbalance.
5) Interpretability: Feature importance / SHAP for clinician-facing insights.

## Notes
- Keep an explicit train/validation/test split to avoid data leakage.
- Track metrics and experiment configs for reproducibility.
