Bank Account Fraud Detection (XGBoost)

A production-minded ML pipeline that flags fraudulent bank account applications in (near) real time. Built on a 1M-row dataset with 32 features and fairness-aware evaluation using three protected attributes (age group, employment status, % income).
Problem & Goal

Fraudsters submit applications with fake identities/docs, causing financial loss and brand damage.
Goal: maximize fraud capture (recall) while keeping false alarms manageable; ship a scalable, automatable model.
Dataset

Size: ~1,000,000 applications

Features: 32 (+ engineered features)

Protected attributes for fairness: age group, employment status, % income

Fraud rate: ~1.1% (11,029 frauds)

Source: Kaggle/GitHub (as referenced in project brief). 
Model

Algorithms tried: Decision Tree, Random Forest, XGBoost

Winner: XGBoost (best accuracy, robust to overfitting, strong recall).

Class imbalance: handled with imbalance-aware strategy (e.g., scale_pos_weight / sampling).

Feature engineering: 3 important features added (improved lift).Business Impact

Automated, real-time fraud screening at account opening.

High recall reduces fraud losses; manageable FP handled by risk workflows.

Provides actionable insights to improve address verification, employment checks, and risk-based processes. 

Key contributors to fraud risk (insights)

Windows OS, credit risk scores, income levels, short tenure at current address surfaced as high-impact signals.
