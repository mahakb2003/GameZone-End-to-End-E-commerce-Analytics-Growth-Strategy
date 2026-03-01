### GameZone-End-to-End-E-commerce-Analytics-Growth-Strategy

📌 Summary

This project analyzes GameZone’s e-commerce data (2019–2022) to support business decision-making across product, marketing, and finance teams. The objective is to evaluate revenue performance by identifying key trends, patterns, and drivers across products, time, regions, and marketing channels. A structured analysis approach is used to translate raw data into actionable insights, enabling stakeholders to optimize growth strategy, improve marketing effectiveness, and make data-driven product decisions.

🗂️ Data Summary

The analysis is based on two primary datasets:

### 1. Orders Table (Cleaned)

The original orders dataset was cleaned and transformed into a structured format to enable analysis. Key preprocessing steps included timestamp standardization, feature extraction, and categorical cleaning.

Final columns include:
a. USER_ID, ORDER_ID
b. PURCHASE_TS, PURCHASE_TS_CLEANED
c. PURCHASE_YEAR, PURCHASE_MONTH
d. TIME_TO_SHIP, SHIP_TS, REFUND_TS
e. PRODUCT_NAME, PRODUCT_NAME_CLEANED, PRODUCT_ID
f. USD_PRICE
g. PURCHASE_PLATFORM
h. MARKETING_CHANNEL, MARKETING_CHANNEL_CLEANED
i. ACCOUNT_CREATION_METHOD, ACCOUNT_CREATION_METHOD_CLEANED
j. COUNTRY_CODE, REGION
k. DATA_CHECK

### 2. Region Table

A lookup table used to map users geographically.
Columns:

a. COUNTRY_CODE
b. REGION

This table is joined with the orders dataset using COUNTRY_CODE to enable regional analysis.

## 🧹 Data Cleaning Summary  

- Performed data quality checks to identify inconsistencies, missing values, and anomalies across datasets  
- Standardized inconsistent date formats using date functions  
- Cleaned product name inconsistencies through recategorization  
- Handled missing categorical values (marketing channel, account creation method) by labeling as **"Unknown"**  
- Corrected region data using lookup mapping from country codes  
- Removed invalid records (e.g., incorrect 1900 date entries)  
- Retained low-impact missing values (e.g., price, country) for stakeholder validation  
- Identified duplicate order IDs but retained them to avoid unintended data loss  
- Flagged shipping date inconsistencies (ship_ts < purchase_ts) for further investigation

### 📸 EDA Visuals 
![Product Revenue Analysis](.png)
