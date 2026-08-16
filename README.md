# Analystlab-africa-week2-powerbi-Global-Superstore-data_analysis-
Building a Global Superstore dataset report using Microsoft Power Bi 

# 🌍 Global Superstore Sales & Profitability Analysis

## 📊 Project Overview

This project presents an interactive **Business Intelligence and Sales Performance Dashboard** developed using the **Global Superstore dataset** in Microsoft Power BI.

The purpose of the project is to transform raw global retail transaction data into meaningful business insights that can support executive decision-making.

The analysis focuses on:

- Sales performance
- Profitability
- Regional performance
- Customer segments
- Product categories
- Product-level profitability
- Sales trends over time
- Business risks and opportunities
- Management recommendations

The final Power BI dashboard provides interactive KPIs, charts, maps, tables, and filters that allow users to explore business performance from different perspectives.

---

## 🎯 Business Problem

A global retail organisation generates large volumes of transaction data across different markets, regions, customers, products, and time periods.

However, raw transaction data alone does not easily answer important management questions such as:

1. What is the overall sales performance of the company?
2. Which regions generate the highest sales and profit?
3. Which customer segments contribute the most revenue?
4. Which product categories perform best?
5. Which products are the most profitable?
6. What trends can be observed over time?
7. What recommendations should management implement to improve business performance?

### Business Objective

The objective of this project is to develop an interactive Power BI dashboard that answers these questions and converts the Global Superstore transaction data into actionable business intelligence.

---

# 📁 Dataset

The project uses the **Global Superstore dataset**, specifically the `Orders` data for the main sales and profitability analysis.

### Main Dataset

**Global Superstore 2016**

The dataset contains transactional information relating to:

- Orders
- Customers
- Markets
- Regions
- Countries
- Product categories
- Sub-categories
- Products
- Sales
- Quantity
- Discounts
- Profit
- Shipping costs
- Order priority

### Main Fields Used

| Field | Description |
|---|---|
| Row ID | Unique row identifier |
| Order ID | Unique order identifier |
| Order Date | Date the order was placed |
| Ship Date | Date the order was shipped |
| Ship Mode | Shipping method |
| Customer ID | Customer identifier |
| Customer Name | Customer name |
| Segment | Customer segment |
| Country | Customer country |
| Market | Global market |
| Region | Geographic region |
| Category | Product category |
| Sub-Category | Product sub-category |
| Product Name | Product description |
| Sales | Revenue generated |
| Quantity | Number of items sold |
| Discount | Discount applied |
| Profit | Profit generated |
| Shipping Cost | Shipping expense |
| Order Priority | Priority assigned to the order |

---

# 🧹 Data Preparation

Data preparation was performed using **Power Query in Microsoft Power BI**.

The following steps were applied:

### 1. Data Import

The Global Superstore dataset was imported into Power BI using:

`Get Data → Excel → Global Superstore 2016`

### 2. Data Type Correction

Appropriate data types were assigned:

- Order Date → Date
- Ship Date → Date
- Sales → Decimal Number
- Profit → Decimal Number
- Shipping Cost → Decimal Number
- Discount → Decimal Number
- Quantity → Whole Number
- Row ID → Whole Number

### 3. Data Cleaning

The following cleaning activities were performed:

- Reviewed missing values
- Checked duplicate records
- Trimmed unnecessary spaces from text fields
- Standardised categorical fields
- Checked numerical fields for invalid values
- Verified date fields
- Reviewed geographic fields

### 4. Date Table

A dedicated Calendar table was created for time-series analysis.

The Calendar table contains:

- Date
- Year
- Month Number
- Month
- Year-Month

The Calendar table was related to:

`Calendar[Date] → Orders[Order Date]`

### 5. Data Modelling

The `Orders` table serves as the primary fact table.

The Calendar table serves as the date dimension used for:

- Year filtering
- Monthly analysis
- Year-over-year analysis
- Sales trends
- Profit trends

---

# 📌 KPI Definitions

The dashboard contains five major KPI cards.

## 1. Total Sales

**Definition:**  
The total revenue generated from all transactions.

### Dax
DAX
Total Sales =
SUM(Orders[Sales])

## 2. Total Profit
**Definition:**
The total profit generated from all transactions.

```DAX
Total Profit =
SUM(Orders[Profit])

## 3. Total Orders
Definition:
The number of unique orders placed.
```DAX
Total Orders =
DISTINCTCOUNT(Orders[Order ID])

## 4. Average Sales
Definition:
Average sales value generated per unique order.
```DAX
Average Sales =
DIVIDE(
    [Total Sales],
    [Total Orders]
)

## 5. Profit Margin
Definition:
The percentage of sales retained as profit.
```DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)