# Loan Default Risk Analysis (Power BI)

## Overview
This project analyzes loan data to identify key factors that drive loan default.  
It focuses on borrower behavior, loan characteristics, and financial risk patterns to support better lending decisions for cooperative societies and financial institutions.

---

## Problem Statement
Loan default is a major challenge for lending institutions, leading to financial losses and reduced capital for future loans.  
Traditional risk assessment methods are often insufficient.

This project aims to:
- Identify key drivers of loan default  
- Segment borrowers based on risk level  
- Support data-driven loan approval decisions  

---

## Dataset
- **Source:** Kaggle (Lending Club Loan Dataset) 
- **Link:** https://www.kaggle.com/datasets/wordsforthewise/lending-club
- **Size:** Reduced to 150,000 rows for performance optimization  

- **Features:** Over 25 relevant columns including:
  - Loan Amount  
  - Interest Rate  
  - Term  
  - Annual Income  
  - Employment Length  
  - Loan Status  

---

## Data Preparation (Power Query)
- Removed irrelevant and high-null columns  
- Fixed inconsistent data types  
- Cleaned percentage and text fields  
- Standardized categorical values  
- Removed duplicates  

### Derived Features:
- Loan-to-Income Ratio  
- Risk Segmentation (Low, Medium, High)  

---

## Data Modeling

A star schema was implemented to improve performance and enable efficient analysis.

- **Fact Table:**
  - Loans (central table containing all loan transactions)

- **Dimension Tables:**
  - Dim_Date (Date, Month, Year)
  - Dim_Income (Income segmentation)
  - Dim_Loan_Status (Loan outcome classification)
  - Dim_DTI (Debt-to-Income segmentation)

### Relationships
- One-to-many relationships from dimension tables to the fact table
- Enables accurate filtering and interactive reporting in Power BI

This structure ensures:
- Faster query performance  
- Clean data organization  
- Reliable dashboard interactions  

---

## Key Metrics (DAX)
- Total Loans  
- Total Defaulted Loans  
- Default Rate  
- Average Loan Amount  
- Risk Segmentation  

---

## Dashboard Features
- KPI Cards (Total Loans, Default Rate, Avg Loan Amount)  
- Default Rate by Income Level  
- Default Rate by Loan Term  
- Interest Rate vs Default Risk  
- Interactive filters (Income category)  

---

## Key Insights
- Middle-income borrowers show the **highest default rate (~6.9%)**  
- Short-term loans (40 months) have **higher default risk** than long-term loans  
- Default risk **increases significantly with higher interest rates**  
- Low-income borrowers show lower default rates, possibly due to smaller loan sizes  

---

## Recommendations
- Apply stricter credit checks for **middle-income borrowers**  
- Limit exposure to **high-interest loans**  
- Encourage **longer repayment terms** to reduce default risk  
- Implement **risk-based loan approval policies**  
- Monitor high-risk segments using automated dashboards  

---

## Tools & Technologies
- Power BI  
- Power Query  
- DAX  

---

## Business Impact
This project helps:
- Reduce loan default risk  
- Improve credit decision-making  
- Identify high-risk customers early  
- Enhance financial sustainability for cooperative societies  

---

## Project Status
✅ Completed  
