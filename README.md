# Financial Risk Assessment and Loan Approval Modeling

### Overview

This project aims to assess and mitigate risks associated with lending by predicting loan defaults and approvals using machine learning.

#### Goals

1. **Risk Score Regression:** Predict a continuous risk score associated with the likelihood of loan default or financial instability.
2. **Binary Classification:** Predict loan approval (approved/denied).
    
### Dataset

The dataset consists of 20,000 records of personal and financial data, including columns such as:

- Demographic information (e.g., age, education level, marital status)
- Financial data (e.g., credit score, debt-to-income ratio, loan amount)
- Loan application data (e.g., loan duration, previous loan defaults)

#### Columns in the Dataset:
- **ApplicationDate:** The date the loan application was submitted.
- **Age:** Applicant's age.
- **AnnualIncome:** Applicant's yearly income.
- **CreditScore:** Creditworthiness score.
- **EmploymentStatus:** Employment status of the applicant (e.g., employed, self-employed, unemployed).
- **EducationLevel:** Highest level of education attained.
- **Experience:** Applicant's years of work experience.
- **LoanAmount:** The requested loan amount.
- **LoanDuration:** The duration of the loan in months.
- **MaritalStatus:** Marital status of the applicant (e.g., single, married, divorced).
- **NumberOfDependents:** Number of dependents in the applicant's household.
- **MonthlyDebtPayments:** Monthly debt obligations.
- **CreditCardUtilizationRate:** Credit card usage percentage.
- **DebtToIncomeRatio:** Ratio of the applicant’s debt to income.
- **LoanApproved:** Binary outcome variable indicating whether the loan was approved (1) or denied (0).
- **RiskScore:** A risk assessment score for each applicant.

### Challenges and Limitations

- **Imbalanced Classes**: The loan approval status (LoanApproved) is imbalanced, with more denials than approvals. We handle this through resampling techniques like SMOTE, but it still affects model performance.
- **Feature Correlation**: Some features like AnnualIncome and MonthlyIncome might be highly correlated, which could impact the model’s predictive performance.
- **Interpretability**: While Random Forest provides good accuracy, its interpretability is limited compared to simpler models, which could be important for understanding loan decisions.

### Future Work

- **Model Improvement**: Try different models such as XGBoost, Logistic Regression, and Neural Networks to improve accuracy.
- **Explainability**: Use SHAP or LIME for model interpretability, making the results more understandable for decision-makers.
- **Deploying the Model**: The final model could be deployed in a real-world system to assist in loan approval processes.
