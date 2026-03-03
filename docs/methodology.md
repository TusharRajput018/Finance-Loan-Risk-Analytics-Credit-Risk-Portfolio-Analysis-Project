# Methodology

## 1. Project Objective

The objective of this project is to analyze loan application data to understand borrower risk profiles, lending patterns, and potential financial exposure.
The analysis supports decision-making in credit risk assessment, loan approval strategies, and revenue estimation for financial institutions.

---

## 2. Data Source

Two datasets were used:

* **Raw Dataset:** `raw_fact_finance.csv`
* **Cleaned Dataset:** `cleaned_fact-finance.csv`

The raw dataset contained loan-level transactional data including borrower demographics, credit characteristics, loan structure, and property information.

---

## 3. Data Understanding

The dataset includes the following categories:

### Borrower Profile

* Gender, Age
* Income
* Credit Score
* Credit Type

### Loan Characteristics

* Loan Amount
* Term
* Interest Rate
* Loan Purpose
* Loan Type

### Risk Indicators

* Loan-to-Value (LTV)
* Debt-to-Income Ratio
* Credit Worthiness
* Open Credit Status

### Property Information

* Property Value
* Occupancy Type
* Construction Type
* Region

---

## 4. Data Cleaning & Standardization

The following preprocessing steps were performed:

* Renamed inconsistent column headers for clarity
  (e.g., `ID` → `Customer_id`, `dtir1` → `dept_to_income_ratio`)
* Corrected spelling inconsistencies and formatting issues.
* Standardized categorical values for loan purpose, gender, and region.
* Ensured numeric columns were properly typed for calculations.
* Removed ambiguity in financial ratio fields.

This improved usability for modeling and dashboard integration.

---

## 5. Feature Engineering (Derived Metrics)

To enable financial analysis, several analytical columns were created:

### 5.1 Loan Tenure

Calculated loan duration classification based on term to analyze long vs short commitments.

### 5.2 Credit Score Banding

Borrowers grouped into risk categories:

* Low
* Medium
* High
* Very High Credit Quality

This allows segmentation instead of analyzing raw scores.

### 5.3 Risk Bucket Creation

A composite risk label derived using:

* Credit Score
* LTV Ratio
* Debt-to-Income Ratio

Used to identify **High-Risk vs Low-Risk lending segments**.

### 5.4 High LTV Flag

Flag created where:
[
LTV > Threshold
]
to highlight highly leveraged loans.

### 5.5 Debt-to-Income Flag (DITR_Flag)

Used to identify financially stretched borrowers.

### 5.6 Estimated Interest Income

[
Interest\ Income = Loan\ Amount \times Interest\ Rate \times Tenure
]
Provides revenue estimation for portfolio analysis.

### 5.7 Monthly Installment Calculation

Derived EMI-style metric to estimate borrower repayment burden.

---

## 6. Analytical Transformation Goals

The transformations were designed to shift the dataset from **transactional format** to **decision-support format**, enabling:

* Risk segmentation
* Profitability estimation
* Lending pattern analysis
* Portfolio monitoring

---

## 7. Data Modeling for Visualization

The cleaned dataset was structured as a fact table for BI tools (Power BI / Excel).

Key modeling considerations:

* All calculated metrics embedded for faster dashboard performance.
* Categorical banding used to simplify slicers and filters.
* Numeric KPIs prepared for aggregation.

---

## 8. Key Analytical Use Cases Enabled

The processed dataset supports:

* Identification of high-risk borrowers
* Regional lending distribution analysis
* Credit score vs loan approval trends
* Revenue forecasting from interest income
* Monitoring leverage through LTV ratios
* Debt burden evaluation across customer groups

---

## 9. Tools Used

* **Python / Excel** — Data Cleaning & Feature Engineering
* **Power BI / Analytical Tools** — Visualization & KPI Modeling
* **CSV Data Processing** — Structured transformation workflow

---

## 10. Outcome

The methodology transformed raw loan-level data into an enriched analytical dataset capable of supporting risk analytics, credit decision frameworks, and financial performance evaluation.
