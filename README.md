# Financial Fraud Detection & Risk Intelligence System

An end-to-end machine learning system for fraud prediction, anomaly detection, transaction risk scoring, alert generation, and Tableau-based fraud investigation.

## Project Overview

This project develops a financial fraud detection and risk intelligence pipeline using supervised machine learning and unsupervised anomaly detection.

The system combines:

- Data quality analysis and exploratory data analysis
- Time-based and transaction-level feature engineering
- Supervised fraud classification
- Class-imbalance handling
- Isolation Forest anomaly detection
- Model validation and comparison
- Fraud probability estimation
- Risk scoring
- Application-level fraud alerts
- Tableau dashboards for investigation and monitoring

## Dataset

The dataset contains 5,000 financial transactions with 14 raw attributes, including:

- Transaction information
- Customer information
- Transaction amount
- Merchant category
- Payment method
- Device type
- Location
- International transaction indicator
- Previous transaction history
- Average customer spend
- Account age
- Fraud target

The target variable is `Fraudulent`.

## Machine Learning

The project evaluates multiple supervised learning models:

- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost

Model performance is evaluated using:

- Accuracy
- Fraud Precision
- Fraud Recall
- F1 Score
- ROC-AUC
- False Positives
- False Negatives

Stratified cross-validation is used to assess model stability and fraud-detection performance.

## Anomaly Detection

Isolation Forest is used as an independent anomaly-detection signal.

The anomaly signal is combined with the final fraud probability to support transaction-level risk scoring.

## Risk Scoring

The final transaction risk score combines:

- 80% Random Forest fraud probability
- 20% anomaly signal

Risk levels are assigned as:

- Low
- Medium
- High
- Critical

High- and Critical-risk transactions are marked for review through the application-level alert mechanism.

## Tableau Dashboards

The project includes three Tableau dashboards:

1. Fraud Risk Executive Overview
2. Fraud Pattern & Intelligence
3. Fraud Risk & Investigation

These dashboards support fraud monitoring, pattern analysis, risk investigation, and high-risk transaction review.

## Project Structure

```text
Financial_Fraud_Risk_Intelligence/
│
├── dashboard/
│   └── Financial Fraud Risk Intelligence.twb
│
├── data/
│   ├── raw/
│   │   └── financial_fraud_detection_dataset.csv
│   └── processed/
│       ├── fraud_alert_log.csv
│       ├── fraud_risk_tableau_data.csv
│       └── tableau_dashboard_data.csv
│
├── notebook/
│   ├── 01_data_audit.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_class_imbalance_handling.ipynb
│   ├── 05_anomaly_detection.ipynb
│   └── 06_risk_scoring.ipynb
│
├── reports/
│   └── Financial Fraud Detection & Risk Intelligence Project Report.pdf
│
├── .gitignore
└── README.md
```bash
git add README.md
git status
