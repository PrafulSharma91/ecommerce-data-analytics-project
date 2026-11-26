# E-Commerce Sales & Customer Analytics

An end-to-end Data Analytics portfolio project analyzing **96,470 delivered orders** (**BRL 15.42M** revenue) across 9 relational tables from the Brazilian Olist E-Commerce dataset. This project uncovers revenue seasonality, logistics bottlenecks, customer retention gaps, and actionable customer segments using Python, SQL, Machine Learning, and Looker Studio.

---

## Live Project Links
- **Interactive 3-Page Dashboard (Looker Studio):** [View Live Dashboard](<https://datastudio.google.com/reporting/cce835cf-493f-4741-a511-81acb003281f>)
- **Full Python & SQL Notebook (Kaggle):** [View Kaggle Notebook](<https://www.kaggle.com/code/praful9174sharma/ecommerce-sales-customer-analytics/edit>)

---

## Tech Stack & Architecture
- **Data Cleaning & Processing:** Python (`Pandas`, `NumPy`) — audited and merged 9 relational CSV tables into a clean order-level master table.
- **Database & SQL Analytics:** `SQLite` — wrote complex analytical queries using **CTEs, Multi-table JOINs, and Window Functions** (`LAG`, `DENSE_RANK`, `SUM OVER`).
- **Exploratory Data Analysis & ML:** `Matplotlib`, `Seaborn`, `Scikit-learn` — performed **RFM Segmentation**, **K-Means Clustering** ($K=4$, Silhouette Score = `0.3939`), and **Cohort Retention Analysis**.
- **Business Intelligence (BI):** `Google Sheets` (pre-aggregated Data Marts) + `Looker Studio` (3-Page Interactive Executive Dashboard).

---

## Key Business Insights
1. **Revenue & Seasonality:**
   - Total delivered revenue reached **BRL 15.42M** across **96,470 orders** with an Average Order Value (AOV) of **BRL 159.83**.
   - Revenue peaked in **November 2017 at BRL 1.15M (+53.54% MoM)** driven by Black Friday, followed by a **-26.89% decline** in December 2017.
2. **Geographic Concentration & Logistics Bottleneck:**
   - Top 3 states (**SP, RJ, MG**) generate **62.54%** of total revenue.
   - While **São Paulo (SP)** maintains a **4.49%** late delivery rate (`4.25` avg review), **Rio de Janeiro (RJ)**—the 2nd largest market—suffers a **12.11%** late delivery rate (`3.97` avg review).
3. **Impact of Late Deliveries on Customer Satisfaction:**
   - Late deliveries crash average customer review scores from **4.29 to 2.27 stars**, with **53.69%** of late orders receiving 1-star ratings.
4. **Customer Segmentation (RFM & K-Means):**
   - **RFM Analysis:** *At-Risk High Value* customers account for **15.51%** of the customer base (14,483 users) but drive **29.15%** of total revenue (avg spend **BRL 310.29**, inactive ~393 days).
   - **K-Means Clustering ($K=4$):** Mathematically isolated **2,801 true repeat VIPs** (avg purchase frequency `2.11`, avg spend **BRL 308.53**).
5. **Retention Crisis (Cohort Analysis):**
   - Overall repeat purchase rate is only **3.00%**, with an average **Month 1 cohort retention rate of 0.45%**.

---

## Actionable Business Recommendations
- **High-Value Win-Back Campaign:** Target the 14,483 *At-Risk High Value* customers with personalized 10–15% discount vouchers via email/WhatsApp to recover high-margin revenue.
- **Carrier SLA Audit:** Renegotiate logistics partnerships in high-delay states (**RJ: 12.11%**, **BA: 12.16%**) and inspect packaging/shipping workflows for high-delay categories like `office_furniture` (`7.97%` late rate, `3.51` avg review).
- **30-Day Post-Purchase Retention Loop:** Trigger automated loyalty coupons within 15–30 days of first delivery to lift Month 1 repeat retention above `0.45%`.

---

## Dashboard Overview (3 Pages)
1. **Page 1 — Executive Summary:** Total Revenue, Orders, AOV, Avg Review KPIs, Monthly Revenue Trend, Late Delivery % vs. Review Score Combo Chart, and Interactive Month Filter.
2. **Page 2 — Product Category & State Performance:** Top Product Categories by Revenue (Horizontal Bar Chart) and State-level Revenue, Orders, Late %, and Review Heatmap Table.
3. **Page 3 — Customer Segmentation (RFM Insights):** Revenue Share Donut Chart, Customer Count by Segment, and RFM Metrics Breakdown Table.
