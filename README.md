📌 Project Title

Kultra Mega Stores (KMS) Inventory and Customer Sales Analysis (2009–2012)

📖 Project Overview

This project involves an end-to-end exploratory data analysis (EDA) of transaction and order data from Kultra Mega Stores (KMS), a Lagos-based retail chain specializing in office supplies and furniture. The objective was to uncover key business insights and support data-driven decision-making for the company's Abuja division. The analysis focuses on sales performance, shipping cost optimization, product demand, customer behavior, and return trends.

🛠 Tools Used

Task

Tool

Data Cleaning

Microsoft Excel

SQL Querying & Analysis

Microsoft SQL Server

Data Visualization

Power BI

Version Control & Portfolio

GitHub

💡 Key Insights from the Analysis

📦 Technology was the product category with the highest total sales.

📍 West and Ontario regions dominated in sales volume.

🚚 Shipping costs were not consistently aligned with order priority—delivery truck was often used for high-priority orders.

🔁 A number of consumer segment customers returned products; most returns occurred in the Office Supplies category.

🏆 The top 5 customers accounted for a significant share of overall revenue, primarily purchasing from Technology and Appliances categories.

🔄 Project Workflow (Step-by-Step)

Data Understanding

Reviewed KMS order dataset (2009–2012) with 21 fields including sales, profit, shipping, product, and customer details.

Reviewed Order Status data to identify returns.

Data Cleaning (Excel)

Removed trailing/leading whitespaces

Replaced "Not Specified" with blanks or proper labels

Standardized date formats (yyyy-mm-dd)

Converted relevant fields to numeric or text as needed

Removed or reviewed nulls and duplicates

Data Import into SQL Server

Created tables and inserted cleaned data

Created a combined view using LEFT JOIN to match order data with return status

Exploratory Data Analysis (SQL)

Answered 11 business questions using advanced SQL queries

Used aggregate functions, filters, joins, and subqueries

Validated business hypotheses (e.g., profitability by customer, shipping cost by priority)

Visualization (Power BI)

Built interactive dashboards:

Sales by Category, Region, Segment

Shipping Cost by Mode and Priority

Returned Orders by Segment

Top/Bottom Customers

Customer behavior insights

Report Documentation (GitHub)

Structured code and visuals in separate folders:

/SQL Queries/ – all .sql scripts

/Power BI Dashboard/ – Power BI .pbix file

/Screenshots/ – images of dashboard insights

Documented SQL queries and dashboard screenshots

Published complete project in portfolio

🧠 Findings and Recommendations

KMS should enforce a logistics policy that aligns shipping mode with order priority to optimize delivery performance and reduce costs.

Low-performing customer segments could be re-targeted with promotions or tailored bundles to boost engagement.

Product bundling strategies and loyalty programs may help increase sales from bottom-tier customers.

Visual analytics revealed opportunities to optimize inventory and focus on high-demand regions and categories.

Return rates suggest a need to improve product quality assurance or customer education for certain categories.
