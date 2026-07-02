# Credit Risk Classification System

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient%20Boosting-green)
![MLflow](https://img.shields.io/badge/MLflow-Experiment%20Tracking-blueviolet)


## Project Overview

Financial institutions process thousands of loan applications every day. Manual credit assessment is often time-consuming, inconsistent, and difficult to scale. This project develops an end-to-end **Credit Risk Classification System** that predicts whether a loan applicant is likely to be a **good credit risk** or a **bad credit risk**, enabling faster and more consistent lending decisions.

The solution covers the complete machine learning lifecycle—from data preprocessing and exploratory data analysis to feature engineering, model training, hyperparameter tuning, experiment tracking with MLflow, and model evaluation.

---

## Business Problem

Traditional loan approval processes require manual verification of customer information, resulting in:

- Slow processing times
- Inconsistent decision making
- Higher operational costs
- Increased financial risk from loan defaults

The objective of this project is to automate credit risk prediction while maintaining strong recall for identifying high-risk applicants.

---

## Project Objectives

- Perform exploratory data analysis on credit applicant data
- Handle missing values and preprocess the dataset
- Engineer informative features
- Train multiple machine learning models
- Optimize model performance using hyperparameter tuning
- Track experiments using MLflow
- Compare models using multiple evaluation metrics
- Select the best model for deployment

---

## Dataset

**Dataset:** German Credit Data

The dataset contains **1,000 loan applications** with demographic, financial, and loan-related attributes.

### Features

- Age
- Sex
- Job
- Housing
- Saving Accounts
- Checking Account
- Credit Amount
- Duration
- Purpose

**Target Variable**

- Risk
  - Good
  - Bad

---

## Repository Structure

```text
Credit-Risk-Classification-System/
│
├── data/
│   └── german_credit_data.csv
│
├── notebooks/
│   ├── 01_EDA_Preprocessing.ipynb
│   ├── 02_Model_Development.ipynb
│   └── 03_Model_Evaluation.ipynb
│
├── models/
│   ├── logistic_regression.pkl
│   ├── decision_tree.pkl
│   ├── random_forest.pkl
│   ├── tuned_random_forest.pkl
│   ├── xgboost.pkl
│   └── tuned_xgboost.pkl
│
├── images/
│
├── reports/
│   └── Project_Report.pdf
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

---

## Project Workflow

```
Raw Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Feature Engineering
      │
      ▼
Train-Test Split
      │
      ▼
Model Training
      │
      ▼
Hyperparameter Tuning
      │
      ▼
Model Evaluation
      │
      ▼
MLflow Experiment Tracking
      │
      ▼
Best Model Selection
```

---

## Data Preprocessing

The preprocessing pipeline includes:

- Missing value handling
- Label Encoding
- One-Hot Encoding
- Standardization
- Stratified Train-Test Split

---

## Feature Engineering

Four additional features were created to improve model performance:

- Credit-to-Duration Ratio
- Age Group
- High Risk Purpose
- Account Stability

These engineered features help capture financial behavior that is not directly represented by the original dataset.

---

## Machine Learning Models

The following classification models were implemented:

- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost

---

## Hyperparameter Tuning

To improve predictive performance:

- **Random Forest**
  - GridSearchCV

- **XGBoost**
  - RandomizedSearchCV

---

## Experiment Tracking

MLflow was used to:

- Track model parameters
- Compare evaluation metrics
- Store trained models
- Save confusion matrix artifacts
- Compare multiple experimental runs

---

## Model Performance

| Model | Accuracy | Precision | Recall | F1 Score |
|--------|----------|-----------|--------|----------|
| Logistic Regression | 0.72 | 0.68 | 0.56 | 0.61 |
| Decision Tree | 0.79 | 0.73 | 0.75 | 0.74 |
| Random Forest | 0.81 | 0.81 | 0.68 | 0.74 |
| Tuned XGBoost | **0.86** | **0.85** | **0.79** | **0.82** |

---

## Best Performing Model

**Tuned XGBoost**

Performance:

- Accuracy: **86%**
- Precision: **84.9%**
- Recall: **78.5%**
- F1 Score: **81.6%**
- AUC-ROC: **0.957**

The tuned XGBoost model demonstrated the best balance between identifying high-risk customers and minimizing false positives, making it the most suitable candidate for deployment.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- MLflow
- Joblib

---

## Installation

Clone the repository

```bash
git clone https://github.com/your-username/Credit-Risk-Classification-System.git
```

Navigate into the project

```bash
cd Credit-Risk-Classification-System
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Project

Execute the notebooks in the following order:

1. 01_EDA_Preprocessing.ipynb
2. 02_Model_Development.ipynb
3. 03_Model_Evaluation.ipynb

---

## Future Improvements

- Address class imbalance using SMOTE
- Deploy the model as a REST API using FastAPI
- Containerize the application using Docker
- Automate retraining with CI/CD pipelines
- Monitor model drift in production
- Develop an interactive dashboard for loan risk analysis

---

