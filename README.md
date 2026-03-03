# Financial Risk Analysis – Credit Risk & Loan Portfolio Analytics

## 1. Project Overview

This project focuses on analyzing financial and credit risk using loan-level customer data. The objective is to assess borrower behavior, evaluate creditworthiness, identify high-risk segments, and support data-driven lending decisions.

The project combines structured data processing, financial risk metrics, segmentation analysis, and business-focused reporting.

---

## 2. Business Objectives

- Analyze customer loan and credit attributes  
- Identify high-risk borrowers using financial indicators  
- Evaluate Loan-to-Value (LTV) and Debt-to-Income (DTI) impact on risk  
- Monitor total portfolio exposure and credit score distribution  
- Support strategic decision-making for loan approvals and risk mitigation  

---

## 3. Problem Statement

Financial institutions often struggle to:

- Detect high-risk borrower segments early  
- Monitor portfolio concentration risk  
- Understand the relationship between credit score, income, and default risk  
- Translate raw loan data into structured risk insights  

Without a clear analytical framework, exposure monitoring and lending decisions become inefficient.

---

## 4. Proposed Solution

This project implements a structured financial risk analytics workflow that:

- Cleans and preprocesses loan data using Python  
- Performs feature engineering (Credit Score Bands, DTI %, LTV %)  
- Develops risk segmentation framework  
- Calculates exposure-based KPIs  
- Generates structured reporting for portfolio risk monitoring  

---

## 5. Dataset Description

The dataset contains approximately 148,000+ loan records including:

- Customer demographic information  
- Loan amount  
- Income level  
- Credit score  
- Debt-to-Income (DTI) ratio  
- Loan-to-Value (LTV) ratio  
- Loan status  
- Region and risk indicators  

Each record represents a unique loan issued to a borrower.

---

## 6. Tools & Technologies

- Python – Data cleaning and transformation (Pandas, NumPy)  
- Jupyter Notebook – Analytical workflow  
- Power BI – Data modeling and portfolio reporting  
- DAX – KPI and risk metric calculations  
- Markdown & PDF – Documentation  
- Git & GitHub – Version control  

---

## 7. Key Analyses Performed

- Credit score segmentation and risk classification  
- DTI and LTV ratio impact analysis  
- Loan exposure and portfolio distribution analysis  
- Regional concentration risk analysis  
- Risk bucket distribution monitoring  

---

## 8. Key Insights

- Credit score and debt-to-income ratio are strong indicators of loan risk  
- High LTV loans show increased exposure and higher default probability  
- Certain regions and demographic segments demonstrate higher concentration risk  
- Portfolio exposure varies significantly across credit score bands  

---

## 9. Data Model Structure

### Fact Table

Fact_Loan

Key Columns:
- Loan ID  
- Loan Amount  
- Credit Score  
- DTI Ratio  
- LTV Ratio  
- Loan Status  
- Region  
- Risk Category  

### Dimension Tables

Dim_CreditScore
- Credit Score Band  
- Risk Classification  

Dim_Region
- Region Name  
- Geographic Category  

Dim_Date
- Year  
- Month  
- Quarter  

Relationships follow a one-to-many structure where dimension tables filter the fact table.

---

## 10. Project Structure
````
Financial_Risk_Analysis_Project/
│
├── data/
│ ├── raw/
│ └── processed/
├── dax/
│ └── measures.md
├── docs/
│ ├── data_dictionary.md
│ ├── business_problem.md
│ └── assumptions_limitations.md
├── powerbi/
│ ├── powerbi_dashboard.pbix
│ └── dashboard_screenshots/
├── python/
│ └── fact_finance_source.ipynb
├── reports/
│ ├── executive_summary.pdf
│ └── insights_report.md
├── requirements.txt
├── .gitignore
└── LICENSE
````

---

## 11. Functional Capabilities

- Risk segmentation  
- Exposure monitoring  
- Financial ratio evaluation  
- Portfolio concentration analysis  
- KPI-based reporting  

---

## 12. Limitations

- Static historical dataset  
- No real-time banking system integration  
- No predictive default probability model implemented  

---

## 13. Future Enhancements

- Develop probability-of-default predictive model  
- Implement automated ETL pipeline  
- Integrate real-time portfolio updates  
- Deploy risk monitoring via Power BI Service  

---

## 13. Dashboard Preview

- Portfolio Overview & Risk Growth Analysis
![image alt](https://github.com/TusharRajput018/Finance-Loan-Risk-Analytics-Credit-Risk-Portfolio-Analysis-Project/blob/7fcd0e1552f47671a1d881272598520db2eb9612/images/dashboard_view1.png)

- Customer Risk Segmentation & Demographic Analysis
![image alt](https://github.com/TusharRajput018/Finance-Loan-Risk-Analytics-Credit-Risk-Portfolio-Analysis-Project/blob/7fcd0e1552f47671a1d881272598520db2eb9612/images/dashboard_view2.png)

- Risk Exposure & Credit Score Impact Analysis
![image alt](https://github.com/TusharRajput018/Finance-Loan-Risk-Analytics-Credit-Risk-Portfolio-Analysis-Project/blob/7fcd0e1552f47671a1d881272598520db2eb9612/images/dashboard_view3.png)

- Income Band & Loan Type Performance Insights
![image alt](https://github.com/TusharRajput018/Finance-Loan-Risk-Analytics-Credit-Risk-Portfolio-Analysis-Project/blob/7fcd0e1552f47671a1d881272598520db2eb9612/images/dashboard_view4.png)

---

## 14. Conclusion

This project demonstrates how structured financial data analysis can transform raw loan records into meaningful credit risk insights.


It provides a scalable analytical foundation for borrower segmentation, exposure monitoring, and data-driven lending decisions.
