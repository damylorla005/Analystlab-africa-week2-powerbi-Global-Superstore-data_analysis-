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

# 🛠️ Tools Used
The following tools were used during the project:

## Microsoft Power BI
Used for:
Data transformation
Data modelling
DAX calculations
KPI development
Data visualisation
Interactive dashboard development

## Power Query
Used for:
Data cleaning
Data transformation
Data type correction
Handling missing values
Removing unnecessary columns
Microsoft Excel / CSV
Used for data inspection and initial review.

## GitHub
Used for:
Project documentation
Portfolio development
Version control
Sharing project files and reports

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


### DAX
Total Sales =
SUM(Orders[Sales])

## 2. Total Profit
**Definition:**
The total profit generated from all transactions.

### DAX
Total Profit =
SUM(Orders[Profit])

## 3. Total Orders
Definition:
The number of unique orders placed.

### DAX
Total Orders =
DISTINCTCOUNT(Orders[Order ID])

## 4. Average Sales
Definition:
Average sales value generated per unique order.

### DAX
Average Sales =
DIVIDE(
    [Total Sales],
    [Total Orders]
)

## 5. Profit Margin
Definition:
The percentage of sales retained as profit.

### DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)

---

# 📦 Product Performance Analysis

The dashboard analyses product and category performance to identify:
Top-performing products
Low-performing products
Best-performing categories
Low-performing categories
Products generating high sales
Products generating low profit
Potential loss-making products
This analysis helps management understand which products are driving business performance and which products require further investigation.
---

# 🌍 Regional Performance Analysis

The project analyses business performance across:
Markets
Regions
Countries
Cities
## The analysis investigates:
Sales by region
Profit by region
High-performing regions
Low-performing regions
Regional growth opportunities
Interactive filters allow users to compare regional performance across different categories and periods.
---

# 📅 Time-Based Analysis
The project includes time-based analysis to investigate business performance over time.

## The analysis focuses on:
Monthly sales performance
Monthly profit performance
High-performing periods
Low-performing periods
Sales trends
Profit trends
Seasonal patterns
This analysis helps identify whether sales and profit are improving, declining or fluctuating over time.
---

# 👥 Customer and Segment Analysis
Customer segment performance is analysed to understand the contribution of different customer groups.

The analysis focuses on:
Sales by segment
Profit by segment
Customer contribution
High-value customers
Most valuable customer segments
This helps identify the customer groups that contribute most to the overall performance of the business.
---

# 🔍 Business Problems Investigated

##Problem 1: 
High Sales but Low Profit
Some products or categories may generate high sales but relatively low profit.
This investigation compares:
Sales
Profit
Quantity
Discount
The purpose is to identify whether strong sales are translating into sustainable profitability.

## Problem 2: 
Loss-Making Products
The project identifies products, categories or sub-categories that generate losses.
The following factors are investigated:
Sales
Profit
Discount
Order volume
Product category

## Problem 3: Regional Underperformance
Some regions or markets may perform below others.
The analysis compares weaker regions with stronger-performing regions to identify:
Performance gaps
Growth opportunities
Potential improvement areas

## Problem 4: Discount Impact
Where discount information is available, the analysis investigates whether higher discounts are negatively affecting profit.
Problem 5: Customer Segment Performance
The project analyses customer segments to identify which groups contribute most to sales and profitability.
---

# 📈 Interactive Dashboard
The interactive Power BI dashboard includes:
KPI Section
Total Sales
Total Profit
Total Orders
Total Units Sold
Profit Margin
Average Sales per Order
Sales and Profit Analysis
Sales trend over time
Profit trend
Sales by category
Profit by category
Product Analysis
Top-performing products
Low-performing products
Category performance
Sub-category performance
Regional Analysis
Sales by market
Sales by region
Profit by region
Customer and Segment Analysis
Sales by customer segment
Profit by customer segment.

## Interactive Filters
The dashboard includes slicers and filters for:
Year
Market
Region
Category
Sub-Category
Customer Segment
These features allow users to interact with the dashboard and explore business performance dynamically.
--- 

#💡 Key Business Insights
The analysis provides important insights into:
The categories and products generating the highest sales.
The products and areas requiring performance improvement.
The regions or markets contributing most to revenue.
The relationship between sales and profitability.
Customer segments that contribute significantly to business performance.
Time periods with strong and weak performance.
Areas where discounts may be affecting profitability.
Replace this section with the exact findings and figures from your final dashboard before publishing.
---
# 💼 Business Recommendations
Based on the analysis, the following recommendations are proposed:
1. Investigate High-Sales, Low-Profit Products
Products generating strong sales but weak profits should be reviewed to identify possible causes such as high discounts or operational costs.
2. Reduce Loss-Making Activities
The business should investigate products, categories and regions generating consistent losses.
Possible actions include:
Reviewing pricing strategies
Reducing excessive discounts
Reviewing costs
Improving product selection
3. Focus on High-Performing Regions
High-performing markets and regions should be analysed to understand the factors driving success.
These strategies can then be applied to underperforming areas where appropriate.
4. Improve Underperforming Regions
Regions with weak sales or profit performance should be investigated to identify growth opportunities.
5. Optimise Discount Strategies
The relationship between discounts and profitability should be monitored.
Discounts should be used strategically to avoid increasing sales while reducing overall profitability.
6. Focus on Valuable Customer Segments
Customer segments contributing significantly to sales and profit should receive targeted marketing and customer retention strategies.
---

# 📁 Project Structure
Global-Superstore-Week3-Analysis/
│
├── data/
│   └── Global_Superstore.csv
│
├── dashboard/
│   └── Global_Superstore_Week3_Dashboard.pbix
│
├── documentation/
│   ├── Advanced_Data_Analysis.pdf
│   ├── Business_Insights_and_Recommendations.pdf
│   ├── DAX_Measures_Documentation.md
│   └── Dashboard_Screenshots.pdf
│
├── images/
│   └── dashboard_preview.png
│
├── README.md
└── LICENSE
---

# 🖼️ Dashboard Preview
Add a screenshot of your completed dashboard here.
Example:
![Global Superstore Dashboard](images/dashboard_preview.png)
---

#🚀 How to Reproduce the Project
Download or clone this repository.
Download the Global Superstore dataset.
Open the .pbix file using Microsoft Power BI Desktop.
Update the data source if required.
Refresh the dataset.
Review the DAX measures.
Interact with the dashboard using the available slicers and filters.
---

# 📚 Skills Demonstrated
This project demonstrates the following skills:
Data Analysis
Business Intelligence
Power BI
DAX
Data Cleaning
Power Query
KPI Development
Data Visualisation
Business Analysis
Data Storytelling
Time-Based Analysis
Profitability Analysis
Product Analysis
Regional Analysis
Business Recommendations
--- 

# 👤 Author
AbdulMalik Mahmood
Data Analytics | Business Intelligence | Power BI | Data Analysis

# 🙏 Acknowledgement
This project was completed as part of the AnalystLab Africa Data Analytics Internship Programme – Week 3.
The project is focused on continuous learning, professional development and building a practical data analytics portfolio.
---

# 📬 Connect With Me
Feel free to connect with me on:

## LinkedIn: https://www.linkedin.com/in/mahmood-abdulmalik-b390202b5?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app
GitHub
## X (Twitter): https://x.com/AbdulMalik89037?t=E1MRyMcy3uaPTiDFzIPdmA&s=09

If you found this project useful, kindly give the repository a ⭐.