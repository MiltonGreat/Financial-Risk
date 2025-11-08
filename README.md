# Financial Risk for Loan Approval

## Overview

In consumer finance, an accurate model is a regulatory and reputational liability if it is a biased one. This project conducts a comprehensive fairness audit of a machine learning system for loan approval, treating bias mitigation not as an optional enhancement but as a core requirement. We demonstrate that high accuracy (92.33%) is meaningless without fairness, and that techniques like adversarial debiasing are essential tools for building models that are both profitable and compliant with fair lending laws like the Equal Credit Opportunity Act (ECOA).

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

The automation of loan approvals promises efficiency but codifies a profound risk: embedding historical biases into scalable, algorithmic decisions. A model that disproportionately denies qualified applicants based on proxies for race, gender, or age isn't just unethical—it's illegal. The dual challenge is to maintain predictive power for credit risk while ensuring equitable outcomes across all demographic groups.

The project addresses the dual challenge of:

- Developing accurate predictive models for loan approvals.
- Ensuring fairness by mitigating biases related to sensitive attributes such as gender, race, and socioeconomic status.

The ultimate goal is to create a model that aligns with ethical standards, enabling fair and equitable decision-making in financial systems.

### Approach: The Algorithmic Compliance Audit

We treated the model development process as a regulatory audit, with bias detection and mitigation as the primary success metrics.

1. **The Pre-Deployment Fairness Audit**

**Disparate Impact Analysis:** We quantitatively tested model outcomes to answer: Does the approval rate differ significantly across sensitive attributes when controlling for legitimate credit factors (e.g., Debt-to-Income Ratio, Credit Score)?

**Bias Mitigation as a Core Step:** We implemented adversarial debiasing and reweighting not as a post-hoc fix, but as an integral part of the model training process. This ensures fairness is "baked in," not "bolted on."

2. **The Explainability & Defensibility Mandate**

**Model Interpretability:** While the Random Forest was the most accurate, we prioritized understanding its decisions. The use of SHAP (SHapley Additive exPlanations) is framed as a compliance necessity, allowing auditors and loan officers to verify that denials are based on legitimate financial factors like Net Worth and Credit Card Utilization, not protected characteristics.

3. **The Multi-Model Governance Panel**

**Comparative Audit:** We didn't settle on a single model. We audited a panel (Logistic Regression, Random Forest) to find the optimal balance between accuracy, fairness, and interpretability, recognizing that different contexts may require different trade-offs.

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

### Audit Results & Compliance Verdict

- Predictive Power - Accuracy: 92.33% (Random Forest)	PASS. The model is highly capable of assessing credit risk based on financial fundamentals.

- Bias Mitigation	- Adversarial Debiasing significantly improved demographic parity. CONDITIONAL PASS. The model meets a higher fairness standard, directly reducing legal and reputational risk.

- Explainability - Random Forest is a "black box" without SHAP. HIGH RISK without XAI. Deployment is not recommended without implementing SHAP/LIME to provide auditable reason codes for every decision.

**Key Governance Finding:** The success of adversarial debiasing proves that fairness and accuracy are not a zero-sum game. The Random Forest model achieved high accuracy while becoming more equitable, making a powerful business case that inclusive lending is also sustainable lending.
    
### Conclusion: The Prognosis for Fair and Profitable Lending

This audit demonstrates that governing an AI for fairness is synonymous with governing it for long-term profitability and regulatory survival.

The path to a compliant and equitable lending AI requires:

1. Mandatory Fairness Testing: Disparate impact analysis must be a non-negotiable step in the model validation lifecycle, with clear thresholds for approval.

2. Explainability by Regulation: Every denial must come with a clear, defensible reason based solely on permissible factors, enabled by tools like SHAP.

3. Continuous Monitoring for Drift: As economic conditions and applicant pools change, the model must be continuously re-audited to ensure fairness is maintained over time.

### Source

https://www.kaggle.com/datasets/lorenzozoppelletto/financial-risk-for-loan-approval
