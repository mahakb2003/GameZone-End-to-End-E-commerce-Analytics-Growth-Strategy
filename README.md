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

## ❓ Business Questions  

### Q1. Revenue Trend Analysis  
How did total revenue across all products perform during 2019–2022?  
Conduct analysis to help product, marketing, and finance teams understand high-level trends.

### Q2. Product-Level Deep Dive  
What was happening in the top 3 products that contributed to the sales dip?

---

## 📊 Initial EDA (Exploratory Data Analysis)

- Analyzed revenue trends across months (2019–2022) to understand overall sales patterns  
- Evaluated product-level performance to identify top and low contributing products  
- Compared category-level contribution to identify underperforming segments  
- Analyzed seasonal trends and time-based spikes in sales  
- Investigated product-wise behavior during peak and dip periods  

---
## 📸 EDA Visuals  
![Product Revenue Analysis](./Screenshot%20(373).png)

---
## 🔍 Key Findings  

- Total sales across 2019–2022 is ~$6.1M, with monthly sales ranging from $80K to $500K  
- Gaming Monitor is the top-performing product (~$2M sales), while Gaming Headset is the lowest (~$800), indicating possible data gaps  
- Headset category contributes <2% of total sales, making it the weakest category  
- Significant spike observed in December 2020, suggesting seasonal or promotional impact  
- Sales increased sharply post-2020 across all products, indicating a macro-level (COVID-driven) trend  
- Consistent spike across products in December 2020, likely driven by campaigns or promotions  
- Flagged shipping date inconsistencies (ship_ts < purchase_ts) for further investigation

