# 📊 Order Analysis Power BI Dashboard

## 🧩 Overview

This project involves analyzing product order data from the past **3 years** using **Power BI Desktop**. The data was sourced from an **Excel file** and processed to build a multi-layered interactive dashboard that helps in understanding order status, delivery timelines, conversion rates, and customer churn.

---

## 🛠️ Design Approach

I have structured the dashboard into **three levels of metrics** for better clarity and data storytelling:

### 🔹 L0 – Summary Metrics (High-Level KPIs)
- **Total Orders**
- **Conversion Rate (%)**
- **Churn Rate (%)**

### 🔹 L1 – Operational Metrics
- Order status breakdown: Disconnected vs Closed vs In-progress
- Delivery performance metrics (80th, 90th, 100th percentiles)
- Company-wise and region-wise delivery comparisons

### 🔹 L2 – Deep Dive Analytics
- Time-based trends in conversion and churn
- Detailed analysis by:
  - `PT_A_CIRCLE`
  - `Company Name`
  - `Year/Month`
- Filters by Company Category, Activity Type, and Year

---

## 📊 DAX Measures Used

```DAX
Total Orders = COUNTROWS('Sheet1')

Conversion Rate (%) = 
DIVIDE(
    CALCULATE(COUNTROWS('Sheet1'), 'Sheet1'[SRF_STATUS] = "SRF --CLOSED"),
    COUNTROWS('Sheet1'),
    0
) * 100

Churn Rate (%) = 
DIVIDE(
    CALCULATE(COUNTROWS('Sheet1'), 'Sheet1'[SRF_STATUS] = "Disconnected"),
    COUNTROWS('Sheet1'),
    0
) * 100

Delivery_80th_By_Company = 
CALCULATE(
    PERCENTILEX.INC(
        VALUES(Sheet1[FAN_NO]), 
        Sheet1[delivery_days],  
        0.8
    ),
    ALLEXCEPT(Sheet1, Sheet1[Company_Name])
)

💡 Key Insights
Total Orders over the past 3 years: 572

Conversion Rate: ~41.43%

Churn Rate (Disconnected orders): 7.52%

Some companies (e.g., ACTWNET, INDISAT) show high churn rates.

Certain regions (e.g., ORISSA, RAJASTHAN) consistently perform well in conversion rates.

Delivery timelines for some companies exceed the 90th percentile, indicating SLA risks.

Fluctuations in conversion rate over time suggest seasonal behavior or process inconsistencies.

✅ Actionable Recommendations
Investigate companies with high churn to improve retention strategies.

Optimize delivery processes for companies exceeding expected delivery timelines.

Deploy targeted interventions in low-conversion regions (e.g., BIHAR, PUNJAB).

Standardize workflows for consistent closure to improve conversion trends.

Analyze churn patterns by Activity Type (Downgrade, Upgrade, DeleteDrops) for root cause analysis.

🔍 Scope for Further Analysis
Rejection Remarks Analysis:
Perform root-cause analysis on orders with rejection or disconnection remarks to identify recurring issues (e.g., incorrect documentation, customer not reachable, pricing issues).
➤ This can be analyzed at each level (company-wise, region-wise, activity type, etc.) to provide targeted corrective actions.

📁 Files
Order_Analysis_Dashboard.pbix – Power BI dashboard file

Order_Data.xlsx – Raw data (last 3 years)

Order_Dashboard_Documentation.md – This documentation
