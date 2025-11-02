# 💳 Credit Card Approval Prediction

This project builds a **machine learning model** to predict whether a credit card application will be **approved or denied** based on applicant data.  
The workflow demonstrates **data preprocessing**, **feature engineering**, and **model evaluation** using **Logistic Regression** and **K-Nearest Neighbors (KNN)**.

---

## 📊 Overview

Financial institutions receive thousands of credit card applications daily.  
This project applies supervised learning techniques to automate approval predictions based on applicant characteristics such as income, debt, employment, and credit history.

---

## 🧩 Dataset

**File:** `cc_approvals.data`  
**Source:** [UCI Machine Learning Repository – Credit Approval Dataset](https://archive.ics.uci.edu/ml/datasets/credit+approval)

| Feature Type | Description |
|---------------|-------------|
| Numerical | Applicant’s age, credit amount, balance, etc. |
| Categorical | Employment type, marital status, ownership, etc. |
| Target | Approval status: **“+” (Approved)** / **“-” (Denied)** |

---

## ⚙️ Workflow Steps

1. **Data Loading & Inspection**
   - Loaded dataset using Pandas.
   - Identified numerical and categorical attributes.

2. **Data Cleaning**
   - Replaced missing values (`?`) with `NaN`.
   - Applied **mean imputation** for numeric features and **mode imputation** for categorical ones.

3. **Encoding & Feature Engineering**
   - Converted categorical columns using **Label Encoding** and **One-Hot Encoding (pd.get_dummies)**.
   - Removed irrelevant or redundant columns.

4. **Data Normalization**
   - Applied **Min-Max Scaling** to normalize features for model training.

5. **Model Building**
   - **Logistic Regression:** Binary classification baseline.
   - **K-Nearest Neighbors (KNN):** Compared performance across `k=1–20`.

6. **Model Evaluation**
   - Evaluated using:
     - **Accuracy Score**
     - **Confusion Matrix**
   - Best Logistic Regression accuracy: **~92.5%**
   - Best KNN accuracy: **~93.8% (k=19)**

---

## 📈 Results Summary

| Model | Accuracy | Notes |
|--------|-----------|-------|
| Logistic Regression | 92.5% | Stable and interpretable baseline |
| KNN (k=19) | 93.8% | Slightly higher accuracy, but costlier in computation |

---

## 🧮 Tools & Libraries

| Library | Purpose |
|----------|----------|
| **Pandas, NumPy** | Data cleaning & manipulation |
| **Scikit-learn** | ML modeling & evaluation |
| **Matplotlib, Seaborn** | Visualization |
| **LabelEncoder, MinMaxScaler** | Preprocessing |

---
