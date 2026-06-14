# 🎯 NGO Donor Retention & Churn Predictor
### Machine Learning Project | NayePankh Foundation Internship Assignment

![Python](https://img.shields.io/badge/Python-3.10-blue)
![ML](https://img.shields.io/badge/ML-XGBoost%20%7C%20Random%20Forest%20%7C%20Logistic%20Regression-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange)

---

## 📌 Project Overview

Non-Governmental Organizations rely heavily on recurring donors to sustain their social impact. A critical challenge is identifying which donors are likely to stop contributing — commonly known as **"donor churn."**

This project builds a complete **Machine Learning pipeline** that:
- Predicts whether a donor will churn based on their behavior
- Compares 3 ML models to find the best performer
- Explains WHY donors churn using SHAP (Explainable AI)
- Quantifies the **financial ROI** of using this model

> 💡 **Key Result:** The model delivers a **775% ROI** — for every ₹1 spent on intervention, NayePankh Foundation saves ₹7.75 in donor revenue.

---

## 📊 Dataset

| Property | Details |
|---|---|
| Source | Publicly available donor behavior dataset |
| Records | 7,043 donors |
| Features | 21 behavioral & demographic features |
| Target | `DonorChurned` (1 = Churned, 0 = Retained) |
| Churn Rate | 26.5% |
| Class Imbalance Handling | SMOTE oversampling |

### Key Features
- `MonthlyDonationAmount` — average monthly contribution
- `MonthsActiveDonor` — how long they have been donating
- `DonationFrequency` — one-time, monthly, or annual donor
- `CommunicationPlatform` — how NGO communicates with them
- `DedicatedSupport` — whether donor has a relationship manager
- `PaymentChannel` — preferred payment method

---

## 🤖 Models Trained & Compared

| Model | Accuracy | F1 Score | ROC-AUC | CV ROC-AUC |
|---|---|---|---|---|
| Logistic Regression | 75.16% | 0.605 | 0.822 | 0.886 ± 0.003 |
| Random Forest | 77.79% | 0.585 | 0.821 | 0.926 ± 0.003 |
| **XGBoost** | **76.79%** | **0.575** | **0.813** | **0.927 ± 0.003** ⭐ |

> **Best Model: XGBoost** — highest and most stable cross-validation ROC-AUC of 0.9272

---

## 📈 Visualizations

The project includes 12 charts:

| Chart | Description |
|---|---|
| Chart 1 | Donor Retention vs Churn Distribution |
| Chart 2 | Monthly Donation Amount & Engagement Duration |
| Chart 3 | Feature Correlation Heatmap |
| Chart 4 | Model Performance Comparison (All 3 models) |
| Chart 5 | ROC Curves — All Models on one plot |
| Chart 6 | Confusion Matrix — XGBoost |
| Chart 7 | Top 10 Feature Importances |
| Chart 8 | 5-Fold Cross Validation Distribution |
| Chart 9 | SHAP Summary Plot — Feature Impact Direction |
| Chart 10 | SHAP Mean Feature Importance |
| Chart 11 | Donor Risk Category Distribution |
| Chart 12 | Cost Benefit Analysis — Revenue Saved vs Lost |

---

## 🔍 SHAP Explainability Insights

Using SHAP (SHapley Additive exPlanations), we identified the **top reasons donors churn:**

1. **MonthlyDonationAmount** — High one-time donors churn more than small recurring donors
2. **DonationFrequency** — One-time donors are significantly more likely to churn
3. **MonthsActiveDonor** — New donors (< 6 months) are the highest risk group
4. **CommunicationPlatform** — Mass digital outreach leads to higher churn than personalized channels

---

## 💰 Cost Benefit Analysis

| Metric | Value |
|---|---|
| At-risk donors identified | 460 |
| Revenue at risk (no model) | ₹20,80,000 |
| Intervention cost | ₹92,000 |
| Donors retained via model | 161 |
| Revenue saved | ₹8,05,000 |
| Net Benefit | ₹7,13,000 |
| **ROI of ML Model** | **775%** |

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| Python 3.10 | Core programming language |
| Pandas | Data manipulation |
| NumPy | Numerical computation |
| Scikit-learn | ML models & preprocessing |
| XGBoost | Gradient boosting model |
| SHAP | Explainable AI |
| Matplotlib | Visualizations |
| Seaborn | Statistical charts |
| Imbalanced-learn | SMOTE for class imbalance |
| Google Colab | Development environment |

---

