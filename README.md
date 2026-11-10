# Credit Risk Early Warning System

A notebook-based machine learning project exploring customer credit risk, repayment behaviour, class imbalance, and default prediction.

## Project overview

Credit risk teams need to identify customers who may miss future payments. This project explores how customer demographics, credit limits, repayment status, billing amounts, and payment history can be used to study credit-card default risk.

The repository contains exploratory analysis and model-validation work in Jupyter notebooks. It is an educational project and should not be treated as a production credit-scoring system.

## Repository contents

| Notebook | Purpose | Dataset |
|---|---|---|
| `Data_Exploration_Validation_and_Cleaning.ipynb` | Data exploration, validation, and cleaning | Give Me Some Credit |
| `Part3_Model_Validation_Class_Imbal_Handling.ipynb` | Credit-card default modelling, validation, and class-imbalance experiments | UCI Default of Credit Card Clients |
| `Siddharth__EWS_project__ProjectSolution_Template.ipynb` | Project solution/template notebook | Review notebook for its detailed scope |
| `Time Series analysis.ipynb` | Separate time-series analysis exercise | Apple stock time-series data |

**Dataset scope:** The repository currently contains work using more than one dataset. The Give Me Some Credit notebook and the UCI credit-card-default modelling notebook are separate analyses; their records and metrics should not be combined.

## Datasets

### 1. Give Me Some Credit

Used in `Data_Exploration_Validation_and_Cleaning.ipynb`.

- Source: [Kaggle — Give Me Some Credit](https://www.kaggle.com/c/GiveMeSomeCredit)
- The notebook loads the `cs-training.csv` file from a public GitHub-hosted copy.
- The data concerns consumer credit and delinquency risk.

### 2. Default of Credit Card Clients

Used in `Part3_Model_Validation_Class_Imbal_Handling.ipynb`.

- Source: [UCI Default of Credit Card Clients](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)
- The notebook loads a CSV copy of the dataset.
- The target column is `default.payment.next.month`.

Important fields include:

| Feature | Description |
|---|---|
| `LIMIT_BAL` | Credit limit |
| `SEX`, `EDUCATION`, `MARRIAGE`, `AGE` | Customer demographic attributes |
| `PAY_0` to `PAY_6` | Recent repayment status |
| `BILL_AMT1` to `BILL_AMT6` | Recent bill statement amounts |
| `PAY_AMT1` to `PAY_AMT6` | Recent payment amounts |
| `default.payment.next.month` | Default outcome (0 or 1) |

## Modelling workflow

The UCI credit-card-default notebook explores the following workflow:

1. Inspect the dataset, columns, data types, and target distribution.
2. Explore categorical, discrete, and continuous variables.
3. Clean and prepare selected features.
4. Train baseline classifiers, including Decision Tree and Logistic Regression.
5. Evaluate predictions using confusion matrices, precision, recall, F1-score, and ROC-AUC.
6. Investigate class-imbalance handling, including oversampling and SMOTE.
7. Compare model behaviour on the held-out test data.

## Technologies

- Python
- Jupyter Notebook
- Pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn
- imbalanced-learn (SMOTE)

## Getting started

### Clone the repository

```bash
git clone https://github.com/siddhu7256/ML-PROJECT-.git
cd ML-PROJECT-
```

### Create and activate a virtual environment

```bash
python -m venv .venv

# macOS / Linux
source .venv/bin/activate

# Windows PowerShell
.venv\\Scripts\\Activate.ps1
```

### Install the notebook dependencies

```bash
python -m pip install jupyter pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

### Launch Jupyter

```bash
jupyter notebook
```

Open the notebook you want to explore. Dataset access may depend on the external URLs used in the notebook; check the dataset source and terms before redistributing any data.

## Planned improvements

- Standardize dataset documentation and make each notebook's data source explicit.
- Move reusable preprocessing and modelling logic into tested Python modules.
- Use stratified train/test splitting before any resampling.
- Put preprocessing and SMOTE inside an imbalanced-learn pipeline to prevent leakage during cross-validation.
- Compare baseline and ensemble models on the same test split.
- Add reproducible experiment configuration and saved evaluation reports.
- Add model explainability and a prediction API after the modelling workflow is validated.

## Author

**Siddharth Kumar**

M.S. Computer Science and Data Analytics

GitHub: [@siddhu7256](https://github.com/siddhu7256)

## Disclaimer

This repository is for educational and experimentation purposes only. It is not validated for real-world lending decisions. Credit decisions require robust validation, fairness assessment, governance, monitoring, and appropriate human oversight.
