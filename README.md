# Nike Global Sales Analysis Dashboard 

## Project Overview
This project analyzes **Nike Inc.'s global sales performance** from **2011 to 2016** across multiple international markets.

The objective was to build an interactive **single-page Power BI dashboard** that provides leadership with centralized visibility into revenue, profit, product performance, sales representatives, and country-level trends.

---

## Business Overview
**Company:** Nike Inc.

Nike Inc. is a global leader in sportswear, footwear, and athletic equipment, operating across six international markets:

- United States
- United Kingdom
- France
- Germany
- Canada
- Australia

The company distributes products across three major categories:

- Bikes
- Clothing
- Accessories

---

## Business Problem
Leadership lacked centralized reporting and visibility into sales performance across countries, product categories, and sales representatives.

### Key Challenges
- No clear view of top-performing vs underperforming sales representatives
- Limited visibility into high-profit product categories
- Untracked country-level revenue imbalances
- No efficient way to monitor year-over-year sales trends

---

## Business Objective
Conduct a structured **6-year global sales analysis (2011–2016)** and develop a Power BI dashboard that enables leadership to:

- Monitor overall sales performance
- Evaluate profitability trends
- Analyze country-level revenue contribution
- Track sales representative performance
- Support strategic business decisions

---

##  Data Dictionary- Nike Global Sales Analysis Dashboard 

This document describes the datasets, fields, and data types used in the
Nike Inc. Sales Performance Analytics Project (2011–2016).

---

### 1. Fact_Sales Table

| Column Name | Description | Data Type |
|-------------|-------------|-----------|
| Order ID | Unique identifier for each customer order (e.g. 1001, 1002) | Whole Number |
| Date | Date the transaction/order was placed | Date |
| Product ID | Unique identifier linking to Dim_Product table (e.g. P01, P02) | Text |
| Rep ID | Sales representative responsible for the sale (e.g. R01, R06) | Text |
| Quantity | Number of units purchased per transaction | Whole Number |

---

### 2. Dim_Rep Table

| Column Name | Description | Data Type |
|-------------|-------------|-----------|
| Rep ID | Unique identifier assigned to each sales representative (R01–R06) | Text |
| Rep Name | Full name of the sales representative | Text |
| Country | Country the sales representative is assigned to | Text |

**Representatives:**
| Rep ID | Rep Name | Country |
|--------|----------|---------|
| R01 | John | United States |
| R02 | Mike | United Kingdom |
| R03 | Anna | Germany |
| R04 | Sophie | France |
| R05 | Liam | Canada |
| R06 | Noah | Australia |

---

### 3. Dim_Product Table

| Column Name | Description | Data Type |
|-------------|-------------|-----------|
| Product ID | Unique identifier assigned to each product (P01–P05) | Text |
| Product Name | Name of the product sold | Text |
| Category | Product classification group | Text |
| Unit Price | Selling price per unit (in USD) | Decimal Number |
| Cost | Cost price per unit (in USD) | Decimal Number |

**Products:**
| Product ID | Product Name | Category | Unit Price | Cost |
|------------|-------------|----------|------------|------|
| P01 | Road Bike | Bikes | $500 | $300 |
| P02 | Mountain Bike | Bikes | $700 | $450 |
| P03 | Helmet | Accessories | $50 | $30 |
| P04 | Gloves | Clothing | $25 | $10 |
| P05 | Jersey | Clothing | $60 | $35 |

---

> **Note:** Revenue, Cost Total, and Profit are calculated columns
> created in Power BI using DAX:
> - `Revenue = Quantity x Unit Price`
> - `Total Cost = Quantity x Cost`
> - `Profit = Revenue - Total Cost`



---

## Data Preparation & Transformation
Data cleaning and transformation were completed in **Power Query Editor**.

### Cleaning Tasks
- Removed inconsistencies and duplicates
- Handled missing values appropriately
- Standardized column formatting
- Assigned correct data types

### Data Modeling
Built relationships between multiple tables for efficient analysis.
<img width="1210" height="675" alt="Image" src="https://github.com/user-attachments/assets/a3a92105-e1a5-4b29-9b50-3a03c46fb363" />

### DAX Measures Created
- Total Revenue
- Total Profit
- Total Orders
- Profit Margin
- Sales Trend Analysis
- Country Contribution Analysis

A dedicated **Calendar Table** was also created using DAX for time intelligence reporting.
<img width="1072" height="737" alt="Image" src="https://github.com/user-attachments/assets/f18e3722-fd3f-4962-9420-cfaa9dbeb44c" />

---

## Tools Used
- Power BI
- Power Query
- DAX
- Excel

  ## Data Visualization
  
  

---

## Key Insights
- Identified top-performing countries driving the highest revenue
- Revealed underperforming sales markets requiring optimization
- Highlighted best-performing product categories
- Tracked multi-year sales growth and profitability trends

---

## Author
**Azeez Akinkunmi Folarin**  
**Role:** Data Analyst  

📧 Email: azeezfola@gmail.com  
📱 Phone: 07080421822  

Open to internships, freelance gigs, and job opportunities.
