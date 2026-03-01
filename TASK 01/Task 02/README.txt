TASK 02: Credit Risk Prediction
OBJECTIVE:
Predict whether a loan applicant is likely to default on a loan.
---
DATASET:
The project uses the Loan Prediction Dataset, which contains information about loan applicants including demographic details, income, loan amount, and credit history.

FEATURES:

* Gender – Applicant gender
* Married – Marital status
* Dependents – Number of dependents
* Education – Graduate or Not Graduate
* Self_Employed – Employment status
* ApplicantIncome – Applicant’s income
* CoapplicantIncome – Co-applicant’s income
* LoanAmount – Requested loan amount
* Loan_Amount_Term – Loan repayment duration
* Credit_History – Previous credit record
* Property_Area – Urban/Semiurban/Rural
* Loan_Status – Target variable (Approved / Not Approved)
---
LIBRARIES:
* Pandas
* NumPy
* Seaborn
* Matplotlib
* Scikit-learn
---
DATA PREPROCESSING:

The dataset contained missing values and inconsistent formats. The following preprocessing steps were performed:

* Replaced special value **"3+"** in the Dependents column with numeric value `3`.
* Converted relevant columns into appropriate numeric formats.
* Missing categorical values were filled using the **mode** (most frequent value).
* Missing numerical values were filled using the **median** to reduce the impact of outliers.
* Categorical variables were encoded into numerical form using Label Encoding.

These steps ensured the dataset was clean and suitable for machine learning models.
---
VISUALIZATION:

Visualizations were created to understand factors influencing loan approval:

* **Loan Status Distribution** – Checked balance between approved and rejected loans.
* **Credit History vs Loan Status** – Showed strong relationship with loan approval.
* **Education vs Loan Status** – Compared approval rates across education levels.
* **Property Area vs Loan Status** – Analyzed geographic influence.
* **Applicant Income vs Loan Status** – Examined income differences using box plots.
* **Loan Amount vs Loan Status** – Compared requested loan sizes.

Visualization helped identify important predictors before model training.
---
MODEL TRAINING:

A **Logistic Regression** classification model was used to predict loan approval.

FEATURE SELECTION:

* Input Features (X): Selected applicant and loan-related attributes.
* Target Variable (y): `Loan_Status`.

The dataset was split into:

* 80% Training Data
* 20% Testing Data
---
MODEL EVALUATION:

### Logistic Regression Results

* **Accuracy:** 0.79 (79%)

### Confusion Matrix

```
[[18 25]
 [ 1 79]]
```

#### Interpretation:

* **True Negatives (18):** Correctly predicted loan rejections.
* **True Positives (79):** Correctly predicted loan approvals.
* **False Positives (25):** Loans predicted approved but actually rejected.
* **False Negatives (1):** Loans predicted rejected but actually approved.

The model performs well in identifying approved applicants but tends to predict approvals more frequently than rejections.

---

## ✅ Conclusion

The credit risk prediction model successfully analyzed applicant information to predict loan approval outcomes. Data preprocessing and visualization helped identify influential factors such as credit history and income. Logistic Regression achieved an accuracy of approximately **79%**, demonstrating effective performance for basic credit risk prediction.

## 🚀 Author

Internship Task – Credit Risk Prediction Project
