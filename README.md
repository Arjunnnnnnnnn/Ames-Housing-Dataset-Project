# Ames Housing Price Prediction

End-to-end regression project predicting **sale prices of homes in Ames, Iowa**
using the well-known Ames Housing dataset. Built with a focus on **clean feature
engineering, linear models, and RMSE-based evaluation**.


## 1. Project Overview

Goal: predict `SalePrice` for residential properties given rich structured data
(79+ features) about the property, location, and condition.



## 2. Dataset

- **Source:** Ames Housing dataset (Kaggle / course-provided version).
- **Target:** `SalePrice` (continuous).
- **Features:** lot area, neighbourhood, house style, overall quality/condition,
  year built/remod, basement & garage features, etc.

Typical preprocessing steps:

- Handle missing values (median/most-frequent, or domain-based fills).
- One-hot encode categorical variables (e.g. neighbourhood, house style).
- Log-transform `SalePrice` and skewed numeric features.
- Standardise numeric features where necessary.


## 3. Methods

- **Baseline models**
  - Simple **mean baseline**.
  - **Plain Linear Regression** on engineered features.

- **Regularised models**
  - **Ridge Regression** (L2) – main workhorse model.
  - **Lasso Regression** (L1) – for feature selection / sparsity.
  - (Optionally) Elastic Net as a compromise.

- **Model selection**
  - Train/validation split or cross-validation.
  - Hyperparameters tuned via `GridSearchCV` on RMSE (or negative MSE).


## 4. Repository Structure


ames-housing-price-prediction/
├─ data/
│  ├─ train.csv
│  └─ test.csv             
├─ notebooks/
│  └─ 01_ames_regression.ipynb
├─ src/
│  ├─ preprocessing.py
│  ├─ models.py
│  └─ evaluation.py
├─ reports/
│  └─ ames_regression_summary.pdf
└─ README.md

