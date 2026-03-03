# 📘 Data Dictionary – Financial Risk Analysis Project

This document provides a detailed description of the variables used in the loan and credit risk dataset.  
Each field is explained in terms of its meaning, expected data type, and relevance to financial risk analysis.

---

## 🧾 Customer & Application Information

| Column Name | Data Type | Description |
|------------|----------|-------------|
| Customer_id | String / Integer | Unique identifier assigned to each customer |
| Year | Integer | Calendar year in which the loan record was created |
| submission_of_application | Categorical | Channel through which the loan application was submitted (e.g., Online, Branch, Agent) |
| age | Integer | Age of the applicant at the time of loan application |
| Gender | Categorical | Gender of the primary applicant |
| Region | Categorical | Geographic region associated with the applicant |

---

## 💰 Loan Details

| Column Name | Data Type | Description |
|------------|----------|-------------|
| Loan_limit | Categorical | Indicates whether the loan falls within standard lending limits |
| Loan_type | Categorical | Structure of the loan such as fixed-rate or variable-rate |
| Loan_purpose | Categorical | Intended use of the loan (e.g., home purchase, refinancing, business use) |
| loan_amount | Numeric | Total loan amount approved for the applicant |
| term | Integer | Duration of the loan expressed in months |
| Loan_Tenure | Integer | Overall repayment period of the loan |
| interest_only | Binary | Indicates whether the loan requires interest-only payments |
| Neg_ammortization | Binary | Specifies if unpaid interest can be added to the principal |
| lump_sum_payment | Binary | Indicates whether lump-sum payments are permitted |

---

## 📊 Interest Rates & Charges

| Column Name | Data Type | Description |
|------------|----------|-------------|
| intrest_rate | Numeric | Interest rate applied to the loan |
| Interest_rate_spread | Numeric | Difference between benchmark rate and applied loan rate |
| Upfront_charges | Numeric | Fees charged at the beginning of the loan |
| Interest_Income_Estimated | Numeric | Estimated interest revenue generated from the loan |
| monthly_installment | Numeric | Monthly repayment amount payable by the borrower |

---

## 🏦 Credit Profile & Risk Indicators

| Column Name | Data Type | Description |
|------------|----------|-------------|
| Credit_Worthiness | Categorical | Overall assessment of the borrower’s credit reliability |
| Credit_Score | Integer | Numerical credit score of the applicant |
| Credit_Score_Band | Categorical | Grouped credit score classification used for risk analysis |
| credit_type | Categorical | Type of credit assessment applied to the applicant |
| co-applicant_credit_type | Categorical | Credit assessment type for the co-applicant, if applicable |
| Risk_Bucket | Categorical | Risk category assigned based on credit and financial factors |
| high_ltv_flag | Binary | Indicates whether the loan has a high Loan-to-Value ratio |
| DITR_Flag | Binary | Indicates whether the Debt-to-Income ratio exceeds acceptable limits |

---

## 🧮 Financial Ratios & Income

| Column Name | Data Type | Description |
|------------|----------|-------------|
| LTV | Numeric | Ratio of loan amount to property value |
| dept_to_income_ratio | Numeric | Proportion of income used to service debt obligations |
| income | Numeric | Annual income reported by the applicant |

---

## 🏠 Property & Collateral Details

| Column Name | Data Type | Description |
|------------|----------|-------------|
| property_value | Numeric | Market value of the property used as collateral |
| construction_type | Categorical | Type of construction of the property |
| occupancy_type | Categorical | Occupancy status of the property (owner-occupied, rental, etc.) |
| Secured_by | Categorical | Asset against which the loan is secured |
| Security_Type | Categorical | Category of collateral provided |
| total_units | Integer | Number of units within the property |

---

## 🏢 Business & Commercial Attributes

| Column Name | Data Type | Description |
|------------|----------|-------------|
| business_or_commercial | Binary | Identifies whether the loan is for business or commercial purposes |
| open_credit | Binary | Indicates the presence of active or open credit lines |
| AIA_Type | Categorical | Loan approval process type (Automated, Assisted, or Manual) |

---

## 📌 Loan Status

| Column Name | Data Type | Description |
|------------|----------|-------------|
| Status | Categorical | Current or final status of the loan (Approved, Rejected, Closed, Defaulted) |

---

## 📝 Additional Notes
- Binary fields are generally represented using **Yes/No** or **1/0**
- Categorical variables may require standardization during analysis
- Numerical fields should be reviewed for missing values and outliers before modeling

---
