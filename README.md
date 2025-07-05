## 📑 Table of Contents

- [Project Topic](#project-topic)
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Project Workflow](#project-workflow)
- [Findings](#findings)
- [Insights and Recommendations](#insights-and-recommendations)
- [Report Documentation](#report-documentation)
📌 Project Topic

Kultra Mega Stores (KMS) Inventory and Customer Sales Analysis (2009–2012)

📖 Project Overview

This project explores historical order data from Kultra Mega Stores (KMS), a Lagos-based retailer of office supplies and furniture. The project was conducted as part of a capstone requirement for the DSA Data Analysis Program. The objective was to uncover trends, customer behavior, and operational insights using data-driven techniques to support strategic decision-making within the Abuja division of KMS.

📂 Data Source

The dataset used for this analysis was downloaded from the Canvas LMS as part of the course materials. Two files were provided:

KMS Sql Case Study.csv – Contains all order and customer transaction records from 2009 to 2012.

Order Status.csv – Contains Order ID of returned orders for the same period.

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

📊 Exploratory Data Analysis

A total of 11 business questions were answered using SQL queries. These covered key performance areas such as:

Product category with the highest sales

Top and bottom 3 sales regions

Appliance sales in Ontario

Customer segmentation and profitability

Most valuable customers

Returned items and shipping efficiency

Each question was backed by SQL queries, and corresponding visualizations were developed using Power BI.

🔄 Project Workflow

Data Cleaning (Excel)

Replaced 'Not Specified' entries with blanks

Standardized date formats (yyyy-mm-dd)

Removed or handled null values

Verified column data types

Data Import (SQL Server)

Created SQL tables and inserted cleaned data

Created a combined view using LEFT JOIN to match orders with return status

EDA & Query Development (SQL)

Wrote individual queries to answer 11 business questions

Grouped, filtered, joined, and aggregated data

Data Visualization (Power BI)

Created bar charts, tables, matrices, pie charts, and KPIs

Used filters and slicers for interactive insights

Focused on customer segments, shipping, and regional sales

Report Documentation (GitHub)

Uploaded SQL scripts for each question: /SQL Queries/

Uploaded .pbix file and exported dashboard screenshots: /Power BI Dashboard/, /Screenshots/

Published a polished README with project narrative

📌 Findings

Office Supplies and Furniture were commonly purchased among low-spending customers.

West and Ontario consistently ranked among the top sales regions.

Most returned items came from the Consumer segment.

Shipping cost was not always aligned with order priority (e.g., delivery trucks used for critical orders).

💡 Insights and Recommendations

Encourage customer loyalty from low-performing customers through promotions, loyalty rewards, and targeted marketing.

Align shipping modes with order priority to improve delivery efficiency and cost control.

Focus on high-performing product categories and top customer segments for upselling opportunities.

Improve product quality and post-sale support to reduce return rates.

📁 Report Documentation

SQL Queries: Answered all 11 case questions using optimized SQL scripts.

Power BI Visuals: Dashboard includes Sales by Category, Top/Bottom Customers, Returns by Segment, and Shipping vs Priority.

Repository Structure:

/SQL Queries/

/Power BI Dashboard/

/Screenshots/

README.md

