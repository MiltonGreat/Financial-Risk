# Financial Risk for Loan Approval

### Problem Statement

Lending institutions need reliable credit scoring models to assess borrower risk and minimize loan defaults.

### Solution Approach

Data: Historical loan datasets with features like income, debt-to-income ratio, credit history, and loan amount.

Methods:

- Preprocessed data to handle missing values and outliers.
- Built classification models (Logistic Regression, Random Forest) to predict loan defaults.
- Performed feature selection to identify key predictors, such as credit score and debt-to-income ratio.
- Addressed class imbalance using oversampling and cost-sensitive learning.
- Tools: Python (Scikit-learn, pandas, Matplotlib).

### Results

- Achieved an accuracy of 87% and an F1-score of 0.85 for default prediction.
- Identified debt-to-income ratio as the strongest predictor of default risk.

### Key Insights

- Credit scoring models built on borrower data can improve lending decisions and minimize risks.
- Feature selection enhances interpretability and model performance.

### Future Directions

- Integrate alternative data sources (e.g., social media behavior, utility bill payments) for fairer credit assessments.
- Deploy the model as an API to automate credit scoring for lenders.

### Overview

The aim of this project is to analyze and predict loan approvals while assessing financial risks associated with borrowers. This involves creating a classification model that predicts whether a loan will be approved (binary classification).

#### Goals

- Clean and preprocess financial and demographic data.
- Engineer meaningful features for better predictive performance.
- Train and evaluate machine learning models.
- Interpret the results to support decision-making in financial risk management.
    
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

### Pipeline

#### Data Preprocessing

- Handled missing values by filling numerical columns with median values and categorical columns with mode.
- Converted date columns into meaningful numeric features (e.g., year, month).
- One-hot encoded categorical variables.
- Standardized numerical features using StandardScaler.

#### Feature Engineering

Created new features such as:
- DebtToIncomeRatio: Ratio of monthly debt payments to annual income.
- NetWorth: Total assets minus total liabilities.

#### Model Training

- Split the data into training (80%) and testing (20%) sets.
- Trained a Random Forest Classifier with balanced class weights to handle class imbalance.

#### Model Evaluation

Evaluated the model using metrics:
- Accuracy: 92.33%
- Precision, Recall, F1-score: Detailed in the classification report.
- ROC-AUC: Assessed model performance on the probability predictions.

#### Key Insights

- High precision for approved loans (1), making the model suitable for reducing false positives in financial risk assessment.
- High recall for non-approved loans (0), ensuring fewer risky approvals.
- The DebtToIncomeRatio and NetWorth were significant features influencing loan approval predictions.

### Future Work

- **Model Improvement**: Try different models such as XGBoost, Logistic Regression, and Neural Networks to improve accuracy.
- **Explainability**: Use SHAP or LIME for model interpretability, making the results more understandable for decision-makers.
- **Deploying the Model**: The final model could be deployed in a real-world system to assist in loan approval processes.

### Source

https://www.kaggle.com/datasets/lorenzozoppelletto/financial-risk-for-loan-approval
