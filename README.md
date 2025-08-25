# Financial Fraud Detection using Machine Learning

A comprehensive system to detect fraudulent transactions in financial datasets using advanced machine learning techniques. This project focuses on **data preprocessing, feature engineering, exploratory data analysis (EDA), and model evaluation**, providing both predictive performance and actionable business insights.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [Models Used](#models-used)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Business Insights & Recommendations](#business-insights--recommendations)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

Financial fraud detection is a critical task for banking and financial institutions. This project implements a machine learning pipeline to **predict fraudulent transactions** and provide insights to prevent financial loss. The workflow includes:

1. Data Loading & Exploration
2. Data Cleaning & Missing Value Handling
3. Feature Engineering & Encoding
4. Handling Class Imbalance (SMOTE)
5. Model Building & Evaluation
6. Correlation & Collinearity Analysis
7. Business Insights & Recommendations

---

## Dataset

The dataset contains transaction records with the following characteristics:

- Features: Transaction type, amount, origin & destination balances, step (time), etc.
- Target: `isFraud` (1 = Fraud, 0 = Non-Fraud)
- Highly imbalanced: Fraud cases are rare compared to non-fraud transactions

**Note:** Ensure the dataset `Fraud.csv` is in the repository or provide a link to a public dataset.

---

## Key Features

- **Feature Engineering:** Balance differences, ratios, transaction hour/day, weekend indicator, etc.
- **Categorical Encoding:** One-hot encoding for transaction types.
- **Outlier Handling:** Outliers are retained as they may indicate fraud.
- **Scaling:** Standardization of numerical features for ML models.
- **Class Imbalance Handling:** SMOTE applied to balance fraud vs non-fraud classes.

---

## Models Used

The following models are implemented and compared:

1. **Logistic Regression** - Fast and interpretable linear model
2. **LightGBM** - Gradient boosting framework optimized for speed and performance
3. **XGBoost** - Gradient boosting library for high predictive accuracy
4. **Naive Bayes** - Probabilistic model (baseline)
5. **Support Vector Machine (SVM)** - Linear kernel for faster training

**Metrics Evaluated:** Accuracy, Precision, Recall, F1-score, AUC-ROC

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/financial-fraud-detection.git
cd financial-fraud-detection
