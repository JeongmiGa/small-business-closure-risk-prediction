# Small Business Closure Risk Prediction

Machine learning project for early detection of small business closure risk using the 2023 MDIS small business survey dataset, with feature engineering, class imbalance handling, threshold tuning, and policy implications.

## Overview
This project analyzes small business closure risk signals using the 2023 MDIS registered small business annual survey data. The goal is not to predict confirmed business closure after the fact, but to detect early warning signals of business discontinuation intent, including business conversion, closure, or retirement plans.

## Problem Statement
Small business closure affects not only individual livelihoods, but also local commercial districts, employment, and policy design. From a practical perspective, early detection of closure risk signals is important for preventive intervention.

## Dataset
- Source: MDIS, 2023 registered small business annual survey data
- Number of businesses: 40,000
- Raw variables: 156
- Final features used for modeling: 118
- Target variable: business continuity intention
  - 0: continue operating
  - 1: business conversion, closure, or retirement plan

## Key Work
- Cleaned and recoded raw survey variables
- Removed low-interpretability and leakage-prone variables
- Created derived variables for better interpretability
- Compared baseline, undersampling, and SMOTE-based Random Forest approaches
- Tuned Random Forest with RandomizedSearchCV
- Optimized classification threshold for imbalanced data
- Interpreted results through feature importance and SHAP-based analysis
- Connected findings to policy implications

## Results
- Best model family: Random Forest
- Final test ROC-AUC: 0.792
- Final test F1-score: 0.270
- Important features included sales, operating costs, operating profit, debt, rent-related costs, business duration, industry, and region.

## Repository Structure
- `notebooks/`: analysis notebook
- `docs/`: written project report
- `data/sample/`: sample data only for structure reference

## Data Notice
The original dataset was obtained from MDIS. This repository currently includes only a sample CSV for structure reference, not the full original dataset. Before publicly uploading the full raw dataset, dataset terms of use and redistribution conditions should be checked.

## Reproducibility
To reproduce the analysis, place the original MDIS dataset file in your local environment and update the file path in the notebook if needed.

## Author
Jeongmi Ga
