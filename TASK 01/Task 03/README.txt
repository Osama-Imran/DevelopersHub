TASK 03: Customer Churn Prediction (Bank Customers)
OBJECTIVE:
Identify customers who are likely to leave the bank.
---
## Libraries Used
- `pandas` — data manipulation
- `numpy` — numerical operations
- `matplotlib` — visualization
- `scikit-learn` — model training and evaluation
---
DATASET:
Source: Churn Modelling Dataset
Records: 10,000 customers
Target Column: `Exited` (1 = churned, 0 = stayed)

FEATURES:
CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary
---
DATA CLEANING:
Removed irrelevant columns: `RowNumber`, `CustomerId`, and `Surname` as they have no predictive value.

ENCODING CATEGORICAL FEATURES:
- `Gender` — Label Encoded (Male/Female → 1/0)
- `Geography` — One-Hot Encoded using `pd.get_dummies()` with `drop_first=True` to avoid the dummy variable trap

TRAIN-TEST-SPLIT:
80% training, 20% testing using `train_test_split` with `random_state=42` for reproducibility.

MODEL TRAINING:
Trained a `RandomForestClassifier` with 100 decision trees (`n_estimators=100`).

MODEL EVALUATION:
- Accuracy: 86.6%
- Strong at predicting customers who stay (recall: 0.97)
- Moderate at catching churners (recall: 0.46) — reflects natural class imbalance in the data

FEATURE IMPORTANCE:
Visualized which features influence churn the most using `model.feature_importances_`.
---
FINDINGS:
- **Age** is the strongest predictor of churn by a significant margin
- **Balance, EstimatedSalary, CreditScore, and NumOfProducts** are all roughly equally important
- **IsActiveMember** — inactive customers are noticeably more likely to churn
- **German customers** churn more than those from France or Spain
- **Gender, HasCrCard, and Geography_Spain** have very little influence on churn

---

RECOMMENDATION:
What I think is that, the bank should focus on retaining older customers with high balances who are becoming inactive, this group represents the highest churn risk.