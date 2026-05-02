# Nike Global Sales Analysis Dashboard 
<img width="1050" height="550" alt="Image" src="https://github.com/user-attachments/assets/ce189719-b23a-4e23-be07-531795766b4f" />
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
Conduct a structured **6 year global sales analysis (2011–2016)** and develop a Power BI dashboard that enables leadership to:

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

  ### Data Visualization
 A single-page interactive **Power BI dashboard** was developed to provide
stakeholders with actionable business insights at a glance.

### Dashboard Features
- **KPI Cards** — Total Cost, Total Profit, Year Cost Avg, Year Profit Avg
- **Line Chart** — Revenue performance over time (monthly trend)
- **Bar Chart** — Profit over time (monthly)
- **Bar Chart** — Country revenue distribution
- **Bar Chart** — Total revenue by product category
- **Donut Chart** — Total cost share by country
- **Slicers** — Filter by Quarter (Q1–Q4) and Year (2011–2016)

<img width="745" height="109" alt="Image" src="https://github.com/user-attachments/assets/b583cc28-4fe6-47da-a54f-0c666a4fd9a8" />
  
  ---
  ## Key Insights
- Identified top-performing countries driving the highest revenue
- Revealed underperforming sales markets requiring optimization
- Highlighted best-performing product categories
- Tracked multi-year sales growth and profitability trends

  ##  Revenue Over Time

### Monthly Revenue Trend (2011–2016)

<img width="251" height="201" alt="Image" src="https://github.com/user-attachments/assets/4b7ac9bb-53f9-49a3-8968-fede7675059e" />

### Sales Trend Insight

Revenue performance fluctuated throughout the fiscal year with a notable
dip in the early months, hovering around the **$100K** mark between
**January and May**.

A strong upward surge was recorded mid-year, with revenue peaking sharply
between **July and September**, exceeding **$150K** — representing the
strongest sales period across the fiscal year.

A significant decline followed after the peak, with revenue dropping back
toward the **$100K** range in **October and November**.

A solid recovery was recorded in **December**, closing the year on an
upward trajectory — suggesting a seasonal pattern characterized by
**strong mid-year performance, a sharp post-peak correction, and a
year-end recovery**.

##  Profit Over Time

### Monthly Profit Trend (2011–2016)

<img width="250" height="206" alt="Image" src="https://github.com/user-attachments/assets/3dac7d8b-71c3-423a-a274-1e2c7d48202b" />

### Profit Trend Insight

Profit remained relatively consistent throughout the year, generally
ranging between **$40K and $50K** across most months, indicating a
stable and healthy margin base.

**January** opened strongly, with profit close to the **$50K** mark
before dipping slightly through **February and March**.

A steady mid year performance was observed from **April through August**,
with profits holding firm in the **$40K–$50K** range.

**September** recorded the highest profit of the year, pushing close to
**$60K** the peak margin period of the fiscal year.

A mild dip was observed in **October and November**, before a strong
**December** recovery closed the year near the **$60K** mark  suggesting
a profit pattern characterized by **consistent mid-year margins, a
September peak, and a strong year-end finish**.


##  Country's Revenue

### Revenue Distribution by Country (2011–2016)

<img width="231" height="207" alt="Image" src="https://github.com/user-attachments/assets/acb6b5b8-71a1-4331-a003-bac4f824982d" />

### Country Revenue Breakdown

| # | Country | Total Revenue |
|---|---------|---------------|
| 1 | France | $289,620 |
| 2 | Canada | $265,875 |
| 3 | Germany | $248,400 |
| 4 | Australia | $243,645 |
| 5 | United Kingdom | $222,505 |
| 6 | United States | $194,255 |

France** leads all markets with the highest revenue, followed closely by **Canada** and **Germany**. The **United States** trails as the lowest-performing market despite being a core territory  signaling a clear opportunity for targeted growth and strategic investment in the US market.

##  Total Revenue by Category

### Revenue Breakdown by Product Category (2011–2016)

<img width="254" height="208" alt="Image" src="https://github.com/user-attachments/assets/0f5732f7-62b6-4bfe-a229-cbb356c34846" />

### Category Revenue Breakdown

| # | Category | Total Revenue | Revenue Share |
|---|----------|---------------|---------------|
| 1 | Bikes | $1,313,300 | 89.7% |
| 2 | Clothing | $93,800 | 6.4% |
| 3 | Accessories | $57,200 | 3.9% |

Bikes** completely dominate revenue at **$1.31M**, dwarfing every other category by a significant margin. **Clothing** and **Accessories** contribute just **6.4%** and **3.9%** respectively  highlighting a heavy product concentration risk. Expanding these two categories through promotions, bundling, and wider product offerings could unlock significant untapped revenue potential.

##  Cost Over Time

### Monthly Cost Trend (2011–2016)

<img width="254" height="207" alt="Image" src="https://github.com/user-attachments/assets/bec4fd36-62f2-4f0d-9508-be29fc1dcf94" />

### Cost Trend Insight

Cost levels remained moderately stable through most of the year,
generally ranging between **$50K and $75K** across the majority of months.

**January** opened with costs around the **$75K** mark before dipping
slightly in **February**, recording one of the lower cost months of
the fiscal year.

A gradual rise was observed from **March through June**, with costs
climbing steadily back toward the **$75K** range as sales activity
increased mid-year.

**September** recorded the highest cost of the year, spiking close to
**$100K**  directly aligned with the revenue and profit peak observed
in the same month.

Costs eased through **October and November** before rising again sharply
in **December**, closing the year near the **$90K** mark suggesting
that cost movement closely mirrors revenue performance, with **high revenue
months consistently driving higher operational costs**.

## 🌐 Total Cost by Country

### Cost Distribution by Country (2011–2016)

<img width="228" height="196" alt="Image" src="https://github.com/user-attachments/assets/a461de87-a61d-4086-9a51-2eef01ed3131" />

### Country Cost Breakdown

| # | Country | Cost Share |
|---|---------|------------|
| 1 | France | 19.80% |
| 2 | Canada | 18.95% |
| 3 | Germany | 16.95% |
| 4 | Australia | 16.72% |
| 5 | United Kingdom | 15.00% |
| 6 | United States | 13.16% |

France** carries the highest cost share at **19.8%**,  consistent with its position as the top revenue-generating market. **United States** records the lowest cost share at **13.16%** — yet also generates the least revenue, suggesting the US market is underperforming relative to its cost efficiency. Markets like **Canada** and **Germany** show strong cost-to-revenue balance, making them the most operationally efficient territories in the portfolio.

##  Recommendations

Based on the six-year global sales analysis of Nike Inc. (2011–2016),
the following recommendations are proposed for leadership consideration:

1. **Invest Heavily in France and Canada** — Both markets lead revenue
at **$289,620** and **$265,875** respectively. Leadership should increase
sales support, rep incentives, and marketing spend in these two territories
to protect and grow their position as the company's top revenue engines.

2. **Develop a Targeted US Growth Strategy** — The United States generates
the lowest revenue at **$194,255** despite carrying a **13.16%** cost share.
A structured intervention including territory expansion, rep performance
reviews, and localized pricing is needed to bring US revenue in line with
its market potential.

3. **Reduce Dependency on Bikes** — Bikes account for **89.7%** of total
revenue, creating extreme product concentration risk. Leadership should
invest in growing the **Clothing** and **Accessories** categories through
targeted promotions, product bundling, and expanded product lines to build
a more balanced and resilient revenue portfolio.

4. **Capitalize on the Mid-Year Sales Window** — Revenue and profit
consistently peak between **July and September**, with revenue exceeding
**$150K** and profit approaching **$60K** in that window. Deploying
focused campaigns, stock builds, and rep incentives ahead of this period
could amplify peak performance and maximize margins.

5. **Monitor and Control September Cost Spike** — While September delivers
the highest revenue and profit, it also drives costs close to **$100K** —
the highest of any month. A cost efficiency review targeting procurement,
logistics, and operational spend during this peak period could significantly
improve net profit margins without sacrificing revenue growth.


---

## Author
**Azeez Akinkunmi Folarin**  
**Role:** Data Analyst  

📧 Email: azeezfola@gmail.com  
📱 Phone: 07080421822  

Open to internships, freelance gigs, and job opportunities.
