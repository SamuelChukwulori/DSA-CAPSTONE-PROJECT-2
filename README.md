# 📑 Table of Contents

- [📌 Project Topic](#-project-topic)
- [📖 Project Overview](#-project-overview)
- [📂 Data Source](#-data-source)
- [🛠 Tools Used](#-tools-used)
- [📊 Exploratory Data Analysis](#-exploratory-data-analysis)
- [🔄 Project Workflow](#-project-workflow)
- [💡 Insights and Analysis](#-insights-and-analysis)
- [📌 Recommendations](#-recommendations)

---

# 📌 Project Topic

**Kultra Mega Stores (KMS) Inventory and Customer Sales Analysis (2009–2012)**

---

## 📖 Project Overview

This capstone project explores historical transactional data from Kultra Mega Stores (KMS), a leading Lagos-based retailer of office supplies and furniture. The goal was to perform an in-depth analysis of customer behavior, regional performance, shipping practices, and return patterns to drive strategic decision-making for the company's Abuja division. Eleven business questions were answered using SQL, and key insights were visualized in Power BI.

---

## 📂 Data Source

The dataset was provided through the course LMS and contains:

- `KMS Sql Case Study.csv` — Detailed customer order and transaction records (2009–2012)
- `Order Status.csv` — A list of returned order IDs during the same period

---

## 🛠 Tools Used

| Task                        | Tool                                    |
|-----------------------------|-----------------------------------------|
| Data Cleaning               | Microsoft Excel[Download Here](https://www.microsoft.com/en-us/microsoft-365/p/excel/CFQ7TTC0HR4R?activetab=pivot:overviewtab)        |
| SQL Querying & Analysis     | Microsoft SQL Server[Download here](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)   |
| Data Visualization          | Power BI[Download Here](https://go.microsoft.com/fwlink/?LinkId=2240819&clcid=0x409&culture=en-us&country=us)               |
| Portfolio Hosting           | GitHub  [Download Here](https://github.com/)               |

---

## 📊 Exploratory Data Analysis

A total of **11 business questions** were answered using SQL. These included:

- Product category with the highest sales
- Top 3 and bottom 3 performing regions by total sales
- Appliance sales in Ontario
- Analysis of the 10 least profitable customers
- Most valuable customers and what they purchase
- Most profitable customer by segment
- Most returning customers and their segments
- Shipping cost vs Order Priority analysis

Power BI visuals were used to display:

- Sales by Region and Product Category
- Top/Bottom Customers by Revenue
- Returns by Segment
- Shipping Methods vs Priority

---

## 🔄 Project Workflow

1. **Data Cleaning (Excel)**
   - Handled missing values (e.g., replacing 'Not Specified')
   - Standardized date formats
   - Removed duplicates and corrected data types

2. **Data Import (SQL Server)**
   - Imported both datasets
   - Joined with `LEFT JOIN` to create a combined view of order and return status

3. **SQL Query Development**
   - Used `GROUP BY`, `JOIN`, `TOP N`, `CASE`, and filtering functions to answer business questions

4. **Power BI Visualization**
   - Interactive dashboards created using bar charts, tables, matrices, and KPIs
   - Slicers added for user interactivity (e.g., by Region, Segment, Ship Mode)

5. **Documentation (GitHub)**
   - Structured folders for SQL scripts, dashboard, screenshots
   - Created README.md with complete walkthrough

---

## 💡 Insights and Analysis

### Question 4: Bottom 10 Customers
- The lowest-spending customers were mostly from the **Consumer** and **Home Office** segments.
- Common purchases: **Furniture** and **Office Supplies**
- Total sales ranged from ₦3.77 to ₦25.52
- ``` SQL
  SELECT TOP 10 Customer_Name,Customer_Segment,Product_Category,
  SUM(Sales) AS TotalSales
  FROM [dbo].[KMS Sql Case Study]
  GROUP BY Customer_Name,Customer_Segment,Product_Category
  ORDER BY TotalSales ASC

### Question 11: Shipping Cost vs Order Priority
- Delivery Truck (slowest) was used even for **Critical** and **High-priority** orders.
- Express Air (fastest and most expensive) was frequently used for **Low-priority** shipments.
- Indicates inefficient shipping strategy.
- ``` SQL
  SELECT 
    Order_Priority,
    Ship_Mode,
	COUNT (*) AS Order_Count,
	SUM(Shipping_Cost) AS Total_Shipping_Cost,
	AVG(Shipping_Cost) AS Avg_Shipping_Cost
	FROM [dbo].[KMS Sql Case Study]
	GROUP BY Order_Priority, Ship_Mode
	ORDER BY Order_Priority, Total_Shipping_Cost DESC

### Question 10: Returned Items
- Returns mostly came from **Consumer** segment.
- Top returned categories included **Office Supplies** and **Furniture**
- Suggests need for product or service improvement for this segment.
- ``` SQL
  SELECT DISTINCT k.Customer_Name,
       k.Customer_Segment
  FROM [KMS Sql Case Study] k
  INNER JOIN [Order_Status] o
  ON k.Order_ID = o.Order_ID
  WHERE Status = 'Returned'
- ``` SQL
  SELECT k.Customer_Name,
       k.Customer_Segment,
	  COUNT (*) AS Return_Count
  FROM [KMS Sql Case Study] k
  JOIN [Order_Status] o
  ON k.Order_ID = o.Order_ID
  WHERE Status = 'Returned'
  GROUP BY k.Customer_Name, k.Customer_Segment
  ORDER BY Return_Count DESC
---

## 📌 Recommendations

### 🔹 For Bottom 10 Customers:
- Launch **re-engagement campaigns** (discounts, loyalty offers)
- Bundle commonly bought items (Furniture + Accessories)
- Assign **sales reps** to underperforming small business accounts
- Use feedback tools to uncover purchase barriers

### 🔹 For Shipping Optimization:
- Implement a **Shipping Policy Matrix** to align ship mode with order priority
- Use automation or training to reduce use of Express Air for non-urgent orders
- Monitor shipping cost patterns monthly

### 🔹 For Reducing Returns:
- Focus on quality control for Office Supplies and Furniture categories
- Educate customers via product guides and after-sale support
- Track return frequency by segment and region to identify trends

---

