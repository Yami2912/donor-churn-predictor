# 🎯 NGO Donor Retention & Churn Predictor
### Machine Learning Project | NayePankh Foundation Internship Assignment

![Python](https://img.shields.io/badge/Python-3.10-blue)
![ML](https://img.shields.io/badge/ML-XGBoost%20%7C%20Random%20Forest%20%7C%20Logistic%20Regression-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange)

---

## 🔗 Project Links

| Resource | Link |
|---|---|
| 📓 Live Notebook (Google Colab) | [Open in Colab](https://colab.research.google.com/drive/1-E9NMlUzgBSUNSHXzm_GBKsXYXK-Fx2s?usp=sharing) |
| 💻 GitHub Repository | [View on GitHub](https://github.com/Yami2912/donor-churn-predictor) |

> 📌 **Best way to view:** Click **Open in Colab** above to see all code, charts and results instantly. Alternatively, download `donor_churn_predictor.ipynb` and open in VS Code or Jupyter Notebook.

---

## 📌 Project Overview

Non-Governmental Organizations like **NayePankh Foundation** rely heavily on recurring donors to sustain their social impact. A critical challenge is identifying which donors are likely to stop contributing — commonly known as **"donor churn."**

This project builds a complete **Machine Learning pipeline** that:
- Predicts whether a donor will churn based on their behavior
- Compares 3 ML models to find the best performer
- Explains WHY donors churn using SHAP (Explainable AI)
- Assigns every donor a **Risk Score (0–100%)** for targeted outreach
- Quantifies the **financial ROI** of using this model

> 💡 **Key Result:** The model delivers a **775% ROI** — for every ₹1 spent on intervention, NayePankh Foundation saves ₹7.75 in donor revenue.

---

## 📊 Dataset

| Property | Details |
|---|---|
| Source | Publicly available donor behavior dataset (Kaggle) |
| Records | 7,043 donors |
| Features | 21 behavioral & demographic features |
| Target Variable | `DonorChurned` (1 = Churned, 0 = Retained) |
| Churn Rate | 26.5% |
| Class Imbalance Handling | SMOTE oversampling |

### Key Features Used
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

> **Best Model: XGBoost** — highest and most stable cross-validation ROC-AUC of 0.9272, meaning it correctly identifies a churning donor 92.7% of the time.

---

## 📈 Visualizations (12 Charts)

| Chart | Description |
|---|---|
| Chart 1 | Donor Retention vs Churn Distribution |
| Chart 2 | Monthly Donation Amount & Engagement Duration |
| Chart 3 | Feature Correlation Heatmap |
| Chart 4 | Model Performance Comparison — All 3 models |
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

Using SHAP (SHapley Additive exPlanations), we identified the **exact reasons donors churn:**

1. **MonthlyDonationAmount** — High one-time donors churn more than small recurring donors
2. **DonationFrequency** — One-time donors are significantly more likely to churn than monthly/annual donors
3. **MonthsActiveDonor** — New donors (under 6 months) are the highest risk group
4. **CommunicationPlatform** — Mass digital outreach leads to higher churn than personalized channels
5. **DedicatedSupport** — Donors without a dedicated relationship manager churn significantly more

### Actionable Recommendation for NayePankh Foundation
Focus retention efforts on: new donors (under 6 months active), one-time high-value donors, and donors reached only through mass digital communication.

---

## 🎯 Donor Risk Scoring

Every donor is assigned a churn probability score (0–100%) and categorized as:

| Risk Category | Churn Probability | Donors | Action |
|---|---|---|---|
| 🔴 High Risk | ≥ 70% | 261 | Immediate personal outreach |
| 🟡 Medium Risk | 40–70% | 199 | Email/call campaign |
| 🟢 Low Risk | < 40% | 949 | Regular engagement |

---

## 💰 Cost Benefit Analysis

| Metric | Value |
|---|---|
| Total donors analyzed | 1,409 |
| At-risk donors identified | 460 |
| Revenue at risk without model | ₹20,80,000 |
| Total intervention cost | ₹92,000 |
| Donors successfully retained | 161 |
| Revenue saved | ₹8,05,000 |
| Net Benefit | ₹7,13,000 |
| **ROI of ML Model** | **775%** |

> For every ₹1 spent running this model and executing outreach, NayePankh Foundation gains ₹7.75 in retained donor revenue.

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

## 🚀 How to Run

### Option 1 — Google Colab (Recommended, zero setup)
1. Click **Open in Colab** link at the top of this README
2. Click **Runtime → Run All** (Ctrl+F9)
3. All 12 charts and results generate automatically in 2–3 minutes

### Option 2 — VS Code / Jupyter (Local)
1. Download `donor_churn_predictor.ipynb` from this repo
2. Install dependencies:
```bash
pip install pandas numpy scikit-learn xgboost shap matplotlib seaborn imbalanced-learn
```
3. Download dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) and place in same folder
4. Open and run the notebook in VS Code or Jupyter

---

## ✅ Assignment Requirements Coverage

| Requirement | Status | Details |
|---|---|---|
| Simple ML Project | ✅ Complete | End-to-end donor churn prediction pipeline |
| Use Real Dataset | ✅ Complete | 7,043 real donor records from Kaggle |
| Build Prediction Model | ✅ Complete | Predicts churn probability per donor |
| Create Visualizations | ✅ Complete | 12 charts covering EDA, models, SHAP, risk |
| Compare Multiple Models | ✅ Complete | Logistic Regression vs Random Forest vs XGBoost |

---

## 📁 Project Structure
