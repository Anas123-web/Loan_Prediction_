# 🏦 Loan Approval Prediction

This project predicts whether a loan application will be approved or not based on customer details such as gender, marital status, income, credit history, and loan amount.  
It was created as part of an **Analytics Vidhya Hackathon** challenge.

---

## 📘 Project Overview

The goal of this project is to build a machine learning model that accurately predicts **Loan Approval Status (Y/N)**.  
The dataset includes both categorical and numerical features related to applicants’ financial and personal information.

---

## 🧩 Dataset Description

The dataset contains the following key columns:

| Feature | Description |
|----------|-------------|
| Loan_ID | Unique Loan Identification Number |
| Gender | Applicant Gender (Male/Female) |
| Married | Marital Status |
| Dependents | Number of Dependents |
| Education | Education Level |
| Self_Employed | Employment Status |
| ApplicantIncome | Monthly Income of Applicant |
| CoapplicantIncome | Monthly Income of Co-applicant |
| LoanAmount | Loan Amount (in thousands) |
| Loan_Amount_Term | Term of Loan (in months) |
| Credit_History | Credit History (1 or 0) |
| Property_Area | Urban/Semiurban/Rural |
| Loan_Status | Target variable (Y/N) |

---

## 🧼 Data Cleaning & Preprocessing

- Handled **missing values**:
  - Used **median** for numerical columns.
  - Used **mode** for categorical columns.
- Created new features:
  - `TotalIncome = ApplicantIncome + CoapplicantIncome`
  - `EMI = LoanAmount / Loan_Amount_Term`
  - `DebtIncomeRatio = (LoanAmount / TotalIncome)`
- Performed **log transformation** on skewed features (`LoanAmount`, `TotalIncome`).
- Encoded categorical variables using **LabelEncoder** and **OneHotEncoder**.

---

## 🤖 Model Building

### Models Tried
- **Logistic Regression**
- **Decision Tree Classifier**
- **Random Forest Classifier** ✅ (Best Performing)

### Final Model
- Model Used: `RandomForestClassifier(random_state=42)`
- Accuracy: **83.74%**
- Cross-validation (5-fold): Stable and consistent results.

---

## 📈 Evaluation Metrics

- Accuracy Score
- Confusion Matrix
- Cross-Validation Score
- Model performance checked on **train-test split (80:20)**

---

## 📊 Tools and Libraries Used

- **Python 3.12**
- **pandas**, **numpy**
- **matplotlib**, **seaborn**
- **scikit-learn**
- **Jupyter Notebook**

---

## 📂 Project Files

| File Name | Description |
|------------|-------------|
| `train_ctrUa4K.csv` | Training dataset |
| `test_lAUu6dG.csv` | Test dataset |
| `loan_prediction.ipynb` | Jupyter notebook for full workflow |
| `loan_prediction.py` | Python script file (for submission) |
| `submission.csv` | Final prediction output file |
| `README.md` | Project documentation |

---

## 🚀 How to Run the Project

1. Clone the repository or download the files.
2. Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
# Loan_Prediction_
