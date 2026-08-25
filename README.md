# atliq-hardwares-sales-analysis

> End-to-end sales analytics project built in Microsoft Excel, transforming raw sales data into a structured data model and decision-ready business reports.

![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-blue)
![Power Pivot](https://img.shields.io/badge/Power%20Pivot-Data%20Modeling-orange)
![DAX](https://img.shields.io/badge/DAX-Analysis-lightgrey)

Completed as part of the **Codebasics Data Analytics Job Simulation Bootcamp**.

---

## Table of Contents

- [Business Context](#business-context)
- [Objective](#objective)
- [Dataset](#dataset)
- [Tools & Techniques Used](#tools--techniques-used)
- [Approach](#approach)
- [Reports & Key Insights](#reports--key-insights)
---

## Business Context

AtliQ Hardware manufactures and sells hardware products such as PCs, mice, and printers through retail and e-commerce channels.

Leadership needed a reliable way to track net sales performance against targets, evaluate customer and product performance, and support annual sales negotiations and discount decisions.

The challenge was to transform raw, unclean transactional data spread across multiple files into structured, reliable analysis that could support business decisions.

---

## Objective

Build a set of clean, decision-ready Excel reports to answer key business questions:

- Which customers are driving sales growth?
- Which markets are meeting or missing their targets?
- Which products are driving sales?
- Which divisions are growing the fastest?
- Which products have the highest and lowest sales volumes?
- Which new products were introduced in 2021?
- Which countries generated the highest net sales in 2021?

---

## Dataset

Raw data was provided as separate CSV files and loaded using **Power Query's Get Data from Folder** functionality.

The datasets were organized into a Star Schema consisting of:

| Table | Description | Key |
|---|---|---|
| `dim_customer` | Customer master data | `customer_code` |
| `dim_market` | Country/market information | `market` |
| `dim_product` | Product master data | `product_code` |
| `fact_sales_monthly` | Monthly net sales and quantity sold | — |
| `dim_date` | Calendar and fiscal-year information | `date` |

AtliQ Hardware follows a **September–August fiscal year**, so a custom `dim_date` table was created to correctly categorize transactions into fiscal years.

---

## Tools & Techniques Used

### Microsoft Excel

- Excel Tables
- PivotTables
- Conditional Formatting
- Custom number formatting
- Interactive filters/slicers
- Report formatting
- PDF export

### Power Query

Used for the complete ETL process:

- Extracting data from CSV files
- Transforming raw datasets
- Cleaning inconsistent values
- Handling blank/NaN values
- Correcting data types
- Preparing datasets for modelling

Examples of data-cleaning steps included:

- Correcting inconsistent labels such as `AttiQ Exclusive` → `AtliQ Exclusive`
- Replacing blank/NaN values with `NA`
- Converting negative quantity values to absolute values
- Validating unique primary keys

### Power Pivot & Data Modelling

- Star Schema
- Fact and dimension tables
- Table relationships
- Data Model
- `RELATED()` for retrieving attributes across connected tables

### DAX

Created reusable measures using:

- `SUM()`
- `CALCULATE()`
- `DIVIDE()`

These were used for year-specific calculations, growth percentages and target-achievement analysis.

### Report Design

- Values displayed in millions for easier interpretation
- Consistent typography and branding
- Conditional formatting
- Three-colour scales
- Data bars
- Company branding and logo
- PDF-ready reports

---

## Approach

### 1. Understand the Business Requirement

Identified the business question each report needed to answer and determined the required fields, filters and measures.

### 2. Extract the Data

Imported the source CSV files into Excel using Power Query.

### 3. Clean & Validate

Prepared the datasets by:

- Correcting inconsistent labels
- Handling missing values
- Checking data types
- Validating primary keys
- Removing potential data-quality issues

### 4. Build the Data Model

Connected the fact and dimension tables using relationships and structured the model using a Star Schema.

### 5. Create the Date Table

Built a custom date table containing month and fiscal-year information to support AtliQ's September–August financial year.

### 6. Create DAX Measures

Developed reusable measures for sales, growth and target-related calculations rather than relying on hard-coded values.

### 7. Build PivotTable Reports

Created individual reports from the Data Model to answer specific business questions.

### 8. Design for Decision-Making

Applied formatting, conditional formatting, filters and consistent branding to make important information easy to identify.

### 9. Export & Present

Final reports were formatted and exported to PDF for business-ready presentation.

---

## Reports & Key Insights

### 1. Customer Performance Report

**Purpose:** Evaluate net sales by customer across FY2019–FY2021 and compare 2021 performance with 2020.

**Business use:** Supports annual sales negotiations and discount decisions.

---

### 2. Market Performance vs Target Report

**Purpose:** Compare actual net sales against market/country-level targets.

**Business use:** Identifies markets that are over- or under-performing against expectations.

---

### 3. Top 10 Products Report

The report ranks products based on their percentage increase in net sales from 2020 to 2021.

- Top 10 product sales in 2020: **$6.43M**
- Top 10 product sales in 2021: **$51.99M**
- Growth: approximately **708%**

The strongest individual growth among the listed products was recorded by **AQ Mx NB**, at approximately **5,624% growth**.

---

### 4. Division Level Report

Overall division sales increased significantly:

- 2020: **$196.69M**
- 2021: **$598.88M**
- Overall growth: approximately **204%**

The **P & A division** generated the highest 2021 sales at approximately **$338.38M**.

The **PC division** recorded the highest year-over-year growth at approximately **314%**.

---

### 5. Top & Bottom 5 Products Report

The report ranks products based on quantity sold and allows analysis by region, division and customer.

**Top 5 products:**

- Combined quantity sold: approximately **19.00M units**
- Highest: **AQ Master wired x1 Ms — 4.15M units**

**Bottom 5 products:**

- Combined quantity sold: approximately **174.89K units**
- Lowest: **AQ HOME Allin1 Gen 2 — 8.85K units**

This comparison highlights the substantial difference in sales volume between the highest- and lowest-performing products.

---

### 6. New Products — 2021 Report

The analysis identified **16 products** introduced in 2021.

Together, these products generated approximately:

**$176.16M in 2021 sales**

The highest-selling new product was:

**AQ Qwerty — $21.98M**

followed by:

**AQ Trigger — $20.74M**

---

### 7. Top 5 Countries by Net Sales — 2021

The top five countries generated approximately:

**$367.22M in combined net sales**

| Rank | Country | Net Sales |
|---|---|---:|
| 1 | India | $161.26M |
| 2 | USA | $87.78M |
| 3 | South Korea | $48.97M |
| 4 | Canada | $35.06M |
| 5 | United Kingdom | $34.15M |

India was the leading country, contributing approximately **44%** of the combined net sales from these five markets.

---

---

## Author

**Sushil Yadav**
Transitioning from 4+ years in equity markets (Kotak Securities, AngelOne) into Data Analytics.

[LinkedIn](https://www.linkedin.com/in/sushil-yadav-880a2a217/) · [GitHub](https://github.com/Sushil2402)
