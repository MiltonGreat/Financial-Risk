# Financial Risk for Loan Approval

## Overview

Lending institutions require effective credit scoring models to assess borrower risk and minimize loan defaults. This project applies machine learning techniques to predict loan defaults based on borrower data. By leveraging classification models such as Logistic Regression and Random Forest, we aim to provide accurate and timely predictions to assist financial institutions in making informed lending decisions. The Random Forest model achieved an accuracy of 92.33%, identifying key risk factors like debt-to-income ratio and net worth to minimize loan default risks.

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

### Problem Statement

Loan approval systems powered by AI can significantly impact individuals' financial opportunities. However, biases in datasets and algorithms can result in unfair decisions, disproportionately disadvantaging underrepresented groups.

The project addresses the dual challenge of:

- Developing accurate predictive models for loan approvals.
- Ensuring fairness by mitigating biases related to sensitive attributes such as gender, race, and socioeconomic status.

The ultimate goal is to create a model that aligns with ethical standards, enabling fair and equitable decision-making in financial systems.

### Solution Approach

#### Data Preprocessing

- Data Cleaning: Addressed missing values by filling numerical columns with median values and categorical columns with mode.
- Feature Engineering: Created new features such as DebtToIncomeRatio and NetWorth.
- Normalization: Standardized numerical features using StandardScaler for better model performance.
- Categorical Encoding: Applied one-hot encoding to categorical variables.

#### Exploratory Data Analysis (EDA)

- Analyzed relationships between key features, such as debt-to-income ratio, credit score, and loan approval status.
- Identified DebtToIncomeRatio and NetWorth as strong predictors of loan approval likelihood.

#### Model Development

- Algorithms Tested: Logistic Regression, Random Forest, and other classifiers.
- Feature Selection: Focused on identifying key predictors, including credit score and debt-to-income ratio.
- Hyperparameter Tuning: Optimized the Random Forest model to improve performance.

#### Model Evaluation

- Accuracy: Achieved an accuracy of 92.33% for loan approval prediction.
- Precision, Recall, F1-Score: Evaluated model performance using detailed classification metrics.
- ROC-AUC: Assessed the model's ability to distinguish between loan approved and denied classes.

### Key Findings

Bias Mitigation:
- Adversarial debiasing significantly reduced bias, resulting in more equitable decision-making.
- Reweighting improved fairness without sacrificing predictive accuracy.

Model Performance:
- Random Forest achieved the highest accuracy and AUC while maintaining fairness.
- Logistic Regression provided interpretable results but required additional fairness adjustments.

Fairness Metrics:
- Demographic parity improved across all models, with fairness constraints ensuring equitable treatment.
- Equalized odds showed balanced false positive and negative rates, particularly in Random Forest and Gradient Boosting models.
    
### Future Directions

- **Model Improvement**: Try different models such as XGBoost, Logistic Regression, and Neural Networks to improve accuracy.
- **Explainability**: Use SHAP or LIME for model interpretability, making the results more understandable for decision-makers.
- **Deploying the Model**: The final model could be deployed in a real-world system to assist in loan approval processes.

### Source

https://www.kaggle.com/datasets/lorenzozoppelletto/financial-risk-for-loan-approval
