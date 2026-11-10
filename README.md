# 💳 Machine Learning-Based Credit Risk Early Warning System

An end-to-end Machine Learning project designed to identify customers with a high probability of credit default and support proactive risk management through predictive analytics.

## 📌 Project Overview

Credit default is a major challenge for financial institutions. Identifying high-risk borrowers before they default can help banks reduce financial losses and improve credit risk management.

This project develops a **Credit Risk Early Warning System (EWS)** using machine learning classification techniques to predict whether a customer is likely to default on their credit card payment.

The system analyzes customer demographics, credit limits, repayment history, billing statements, and previous payment behavior to identify potential defaulters.

## 🎯 Objectives

- Predict the likelihood of customer credit default.
- Identify high-risk customers using historical financial data.
- Address class imbalance using SMOTE.
- Develop and evaluate machine learning classification models.
- Prioritize recall to reduce missed default cases.
- Support data-driven credit risk assessment.

## 📊 Dataset

The project uses the Credit Card Default dataset, containing customer-level financial and demographic information.

**Key features include:**

| Feature | Description |
|---|---|
| LIMIT_BAL | Customer credit limit |
| SEX | Customer gender code |
| EDUCATION | Education category |
| MARRIAGE | Marital status |
| AGE | Customer age |
| PAY_0 to PAY_6 | Historical repayment status |
| BILL_AMT1 to BILL_AMT6 | Monthly billing amounts |
| PAY_AMT1 to PAY_AMT6 | Previous payment amounts |
| Default Target | Indicates whether the customer defaulted |

**Target variable:**
- `0` – No default
- `1` – Default

## 🛠️ Technology Stack

- **Programming:** Python
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Class Imbalance Handling:** Imbalanced-learn (SMOTE)
- **Development Environment:** Jupyter Notebook

## ⚙️ Methodology

The project follows a structured machine learning workflow.

### 1. Data Preprocessing
- Inspected dataset structure and data types.
- Checked for missing values and duplicate records.
- Examined feature distributions and target imbalance.
- Prepared features for model training.

### 2. Exploratory Data Analysis (EDA)
- Analyzed customer demographics.
- Examined repayment patterns.
- Studied billing and payment behavior.
- Identified potential risk indicators.

### 3. Handling Class Imbalance

The dataset contains an imbalanced target distribution, which can lead to biased predictions.

**SMOTE (Synthetic Minority Over-sampling Technique)** was used to address class imbalance by generating synthetic samples for the minority class.

### 4. Model Development

A Decision Tree Classifier was implemented to identify patterns associated with credit default.

The model learns relationships between repayment behavior, credit limits, billing history, and customer characteristics.

### 5. Model Evaluation

The model was evaluated using classification metrics, with particular emphasis on identifying actual defaulters.

Key evaluation metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

## 📈 Results

The implemented Decision Tree classification approach achieved approximately **92% recall for the default class** in the reported experiment.

This indicates that the model successfully identified a substantial proportion of actual defaulters.

**Why recall matters:**

In credit risk management, failing to identify a potential defaulter can result in financial losses. Therefore, recall is an important metric for evaluating early warning systems.

*Note: The reported recall should be accompanied by the test-set evaluation, precision, F1-score and confusion matrix when publishing final results.*

## 🏗️ Project Workflow

```text
Historical Credit Data
        |
        v
Data Preprocessing
        |
        v
Exploratory Data Analysis
        |
        v
Feature Preparation
        |
        v
Train-Test Split
        |
        v
SMOTE (Training Data Only)
        |
        v
Decision Tree Classifier
        |
        v
Model Predictions
        |
        v
Performance Evaluation
        |
        v
Credit Risk Identification
```

## 📁 Project Structure

```text
ML-PROJECT-/
│
├── dataset/
│   └── credit_default.csv
│
├── notebooks/
│   └── credit_risk_analysis.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── train.py
│   └── evaluate.py
│
├── models/
│   └── README.md
│
├── results/
│   └── README.md
│
├── requirements.txt
├── .gitignore
└── README.md
```

*Adjust this structure to match the files actually present in your repository.*

## 🚀 Installation and Usage

### 1. Clone the repository

```bash
git clone https://github.com/siddhu7256/ML-PROJECT-.git

cd ML-PROJECT-
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the environment

```bash
# Windows
venv\Scripts\activate

# Linux / macOS
source venv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the notebook

```bash
jupyter notebook
```

Open the credit risk analysis notebook and execute the cells.

## 🔍 Key Learnings

- Practical application of supervised machine learning.
- Understanding class imbalance in financial datasets.
- Applying SMOTE for minority-class oversampling.
- Evaluating classification models beyond accuracy.
- Understanding the importance of recall in credit risk identification.
- Building a structured machine learning workflow.

## 🔮 Future Improvements

- Experiment with Random Forest, XGBoost and LightGBM.
- Compare models using precision-recall curves and ROC-AUC.
- Implement SHAP for model explainability.
- Add probability calibration and risk segmentation.
- Develop a FastAPI prediction service.
- Build an interactive credit risk monitoring dashboard.
- Integrate model monitoring and data drift detection.

## 👨‍💻 Author

**Siddharth Kumar**

M.S. Computer Science

Interested in Machine Learning, AI Engineering, Generative AI and intelligent financial systems.

- GitHub: [@siddhu7256](https://github.com/siddhu7256)

---

⭐ If you find this project useful, consider giving the repository a star.

*Disclaimer: This project is intended for educational and research purposes. Predictions should not be used as the sole basis for real-world credit decisions.*

