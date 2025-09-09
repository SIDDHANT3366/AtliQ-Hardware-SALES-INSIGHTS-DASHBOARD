📊 AtliQ Hardware Sales Insights Dashboard
📌 Project Overview

This project focuses on building an automated Sales Insights Dashboard for AtliQ Hardware in Power BI. The main objective is to support the Sales Team and related stakeholders in making data-driven decisions, while also reducing manual efforts in data gathering and reporting.

The dashboards provide key insights into Revenue Trends, Profit Analysis, and Performance Metrics, helping uncover patterns and areas of improvement for cost savings and better profitability.

🏷️ Problem Statement

Sales for AtliQ Hardware are declining 📉.
The Sales team lacks a centralized view of insights for quick decision-making.
Manual reporting consumes excessive time ⏳, reducing efficiency.

🎯 Applied AIM’s Grid

Purpose:
To build automated sales dashboards that uncover insights and reduce time in data gathering.

Stakeholders:
Sales Director
Marketing Team
Customer Service Team
Data Analytics Team
IT Team

End Result:
Automated dashboards providing quick & latest sales insights.
Enhanced ability for the sales team to take data-driven decisions.

Success Criteria:
Dashboards uncovering sales order insights with the latest available data.
Sales team achieves 10% cost savings through better decisions.
Sales analysts save 20% of their time, reinvesting it into value-adding activities.

📂 Dataset Details

The dataset contained around 150,000 transactions and 38 customers across multiple markets.

Tables Used:
Customers: customer_code, customer_name, customer_type
Date: date, cy_date, year, month, dd_mm_yy
Transactions: product_code, customer_code, market_code, order_date, sales_quantity, sales_amount, currency
Products: product_code, product_type
Markets: market_code, market_name, zone
Data Cleaning & Transformation Steps:
Removed markets New York and Paris (since ~95% sales are from India).
Removed negative & zero sales amounts.
Standardized all currencies to INR.
Cleaned dimension tables (removed blank zones, normalized columns).

🏗️ Data Modeling

Built a Star Schema connecting dimension tables with the fact table (transactions) using common attributes.
Added calculated measures:
Sales Quantity = SUM(transactions[sales_quantity])
Normalized cy_date to display mmm_yy format in slicers (compact view).

📊 Dashboard Pages

1️⃣ Key Insights

Overall Revenue: ₹985M
Total Profit Margin: ₹24.66M
Sales Qty: 2M
Revenue and Profit insights shown for both Brick & Mortar and E-Commerce customer types.
Revenue Trend line chart for sales across years.

2️⃣ Profit Analysis

Revenue % Contribution by Markets → ~50% revenue comes from Delhi NCR.
Profit % Contribution by Market → Delhi NCR leads (48.5%), followed by Mumbai (19.8%).
Profit % Margin by Market → Surat (4.86%) & Patna (4.12%) are most profitable.
Side-by-side table for customer-wise contribution with revenue, profit, and margin.

3️⃣ Performance Analysis

Revenue by Zone, Market, Customer, and Product (drill-down analysis).
Revenue Trend (column + line chart): compares previous year vs current year revenue, with Profit Margin % overlay.
Profit Target Parameter (slicer): dynamically sets profit margin threshold.
Zones/Markets/Products falling below target margin turn Red for easy identification.
Example: Target set at 3% → Central & North Zones highlighted in red.

📷 Dashboard Snapshots

Key Insights Page → P1.png
Profit Analysis Page → P2.png
Performance Analysis Page → P3.png

✅ Key Learnings & Outcomes

Automated dashboards replaced manual reporting, saving analysts’ time.
Delhi NCR is the biggest revenue contributor but not the most profitable market.
Surat and Patna showed better profit margins, useful for strategy realignment.
Introduced dynamic profit target filtering, enabling performance benchmarking.

🛠️ Tools & Technologies Used

SQL → Data extraction, cleaning, and transformation
Power BI → Data modeling, visualization, dashboard design
Data Modeling Technique → Star Schema

📌 Future Improvements

Add forecasting for revenue and profit trends.
Include customer segmentation analysis for targeted sales strategies.
Automate SQL-Power BI pipeline for real-time updates.

📖 How to Use

Clone this repository.
Open .pbix file in Power BI Desktop.
Connect to dataset (if external DB is required).
Explore dashboards with filters & slicers.
