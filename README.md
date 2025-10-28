# 🏦 Loan Approval Prediction

This project analyzes and predicts loan approval outcomes using **Machine Learning** models — mainly **Logistic Regression** and **Random Forest**.  
It is based on real-world style loan application data and explores which factors most influence loan approval decisions.

---

## 📊 1. Data Cleaning & Preprocessing

- Handled missing values:
  - Replaced missing values in `Married` and `Self_Employed` with `"Unknown"`.
  - Imputed missing `LoanAmount` with the **median**.
- Created income categories by dividing `ApplicantIncome` into:
  - **Low**, **Medium**, **High**, and **Very High**.
- Encoded categorical variables for modeling.

### 🔍 Key Findings
| Feature | Approval Rate |
|----------|---------------|
| Not Married | 62% |
| Married | 71% |
| With Credit History | 79% |
| Unknown Self-Employed | 71% |

➡️ Applicants with *unknown self-employment status* still had a high approval rate — suggesting that this missing information may carry hidden patterns.

---

## 🤖 2. Model Training & Evaluation

Two models were trained and compared:
- **Logistic Regression**
- **Random Forest**

### Results Summary
| Metric | Logistic Regression | Random Forest |
|---------|---------------------|---------------|
| Accuracy | ~0.79 | ~0.77 |
| Strength | Excellent for approvals | More balanced between classes |
| Weakness | Misclassifies rejections | Slightly lower precision |

**Confusion Matrices**
- Logistic Regression correctly predicts most approvals but misses many rejections.
- Random Forest improves balance by reducing false negatives.

---

## 🔎 3. Feature Importance Insights

| Feature | Importance |
|----------|-------------|
| Credit History | Highest influence |
| Applicant Income | Strong impact |
| Loan Amount | Moderate |
| Coapplicant Income | Moderate |
| Demographics (Gender, Education, etc.) | Minor impact |

- The model relies heavily on **Credit History** and **Financial Capacity**.
- **Positive credit history** increases approval odds **3.7×**.
- Being **married** or owning property slightly improves chances.

---



## 📚 References

- Scikit-Learn Documentation: [https://scikit-learn.org/stable/](https://scikit-learn.org/stable/)
- Kaggle Loan Prediction Dataset: [https://www.kaggle.com/datasets/ninzaami/loan-predication](https://www.kaggle.com/datasets/ninzaami/loan-predication)
- Logistic Regression Theory (StatQuest): [https://www.youtube.com/watch?v=yIYKR4sgzI8](https://www.youtube.com/watch?v=yIYKR4sgzI8)

---
