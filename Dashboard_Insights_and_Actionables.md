#Dashboard Insights and Business Recommendations

This document captures the key insights and actionable recommendations derived from the Power BI dashboard built
using the `NPLC_product_report` dataset.

---

## Key Observations

1. **Business KPIs Available at a Glance**
   - The dashboard clearly displays:
     - Total Amount Spent
     - Average Delay in Order Closure
     - Number of Disconnected Orders

2. **Trend of Disconnected Orders**
   - In **2025**, disconnected orders are **decreasing**, which is a **positive indicator** of process
     stabilization or customer retention improvements.

3. **High Average Delay Days**
   - The **average delay** for order closure is around **80 days**.
   - This requires immediate investigation — a standard SLA (Service Level Agreement) such as
      **"close all orders within 40 days"** can be implemented to improve operational efficiency.

4. **Drop in Orders in 2025**
   - There is a noticeable **drop in order count in 2025**.
   - This may indicate a **market shift**, internal issue, or external event.
   - Suggestion: Conduct a root cause analysis for the decline.

5. **Discount vs Closed Orders Relationship**
   - The stacked column + line chart shows a **direct correlation** between **total discount** and **closed orders**.
   - To boost order closures, consider:
     - Increasing discount offerings in **low-performing regions**
     - Running **targeted campaigns** in those areas

6. **Top Performing Companies**
   - A chart displaying **orders by company** highlights the **top 10 companies** contributing the most orders.
   - Suggestion: 
     - Maintain relations with top companies
     - Launch **marketing campaigns** to **boost engagement** with lower-tier companies

---

## Actionable Business Steps

| Area                  | Action Item                                                                 |
|-----------------------|------------------------------------------------------------------------------|
| SLA Policy            | Implement a maximum order closure SLA (e.g., within 40 days)                 |
| Order Drop in 2025    | Perform trend analysis and root cause investigation                          |
| Regional Strategy     | Increase discounts in low-performing regions                                 |
| Customer Segmentation | Design focused outreach for companies with lower order contributions         |
| Efficiency Tracking   | Add KPIs like **Discount Efficiency** or **Closure Rate** by Region/Company  |

---

## 💬 Interview Explanation Snippet

> “My dashboard helped surface key operational insights, such as an 80-day average delay in order closure, and a
positive downward trend in disconnected orders. By comparing total discount and closed orders across regions,
I observed that higher discounts directly led to more closures. This allowed me to recommend increasing discounts in
> underperforming areas. I also built customer-level insights to prioritize marketing toward low-engagement companies. These findings are presented with visual clarity and documented for decision-makers.”

---

