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

**Metrics Evaluated:** Accuracy, Precision, Recall, F1-score, AUC-ROC

---

## Results

| Model                 | Accuracy  | Precision | Recall   | F1-Score | AUC      |
|-----------------------|----------|-----------|---------|----------|----------|
| Logistic Regression   | 0.999891 | 0.923901  | 0.997565 | 0.959321 | 0.999962 |
| LightGBM              | 0.999969 | 0.978507  | 0.997565 | 0.987945 | 0.999921 |
| XGBoost               | 0.999869 | 0.908638  | 0.998783 | 0.951580 | 0.999739 |
| Naive Bayes           | 0.992910 | 0.153796  | 0.997565 | 0.266504 | 0.999039 |

---

## Business Insights & Recommendations

- Monitor specific transaction types: Focus on high-risk types.
- Implement real-time fraud detection: Deploy the best-performing models (LightGBM/Logistic Regression).
- Strengthen verification: Add extra checks for suspicious transactions.
- Regular model retraining: Keep models updated with new data for high accuracy.

**Note:** Naive Bayes has high recall but low precision, meaning it flags many non-fraud transactions as fraud.

---

## Usage

### 1. Create a Virtual Environment

```bash
python -m venv venv  
source venv/bin/activate   # On Windows: venv\Scripts\activate
```
## Installation 

### 2. Installing requirements
```bash
pip install -r requirements.txt
```

### 3. Clone the Repository
```bash
git clone https://github.com/DhruviGaur30/Financial-Fraud-Detection-ML.git
cd Financial-Fraud-Detection-ML
```
### 4. Set up and Usage

1. Place Fraud.csv in the project directory.
2. Run the Jupyter notebook:
3. jupyter notebook fraud_detection_accredian.ipynb
4. Follow the notebook steps to:
-Preprocess the data
-Train multiple models
-Evaluate model performance

---

### License

This project is open-source and available under the MIT License.
