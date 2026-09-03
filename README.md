# 📊 Data Analytics Practice Dataset

A realistic synthetic sales dataset designed for practicing **Power BI, DAX, SQL, Python, and Excel**.

The dataset follows a **star-schema data model** with 20,000 sales transactions, dimension tables, defined relationships, and 40+ DAX practice questions ranging from beginner to advanced.

Whether you're learning data analytics, preparing for interviews, or building portfolio projects, this dataset can be used as a hands-on environment for practicing end-to-end data analysis.

---

## 🎯 Project Overview

This repository provides a reusable dataset for practicing common **Data Analyst and Business Intelligence workflows**, including:

* Data exploration and analysis
* Data modeling
* Star schema design
* Table relationships
* SQL querying
* Excel analysis
* Power BI reporting
* DAX calculations
* Customer and product analysis
* Sales and profitability analysis
* Time-series analysis
* KPI development
* Ranking and Top-N analysis

The dataset is intentionally designed to work across multiple analytics tools rather than being limited to Power BI.

---

## 📦 What's Included

### Excel Workbook

**`Power_BI_DAX_Practice_Dataset.xlsx`**

The workbook contains:

| Table         | Description                   |
| ------------- | ----------------------------- |
| `FactSales`   | Sales transaction fact table  |
| `DimDate`     | Date/calendar dimension       |
| `DimProduct`  | Product attributes            |
| `DimCustomer` | Customer attributes           |
| `DimStore`    | Store and regional attributes |

The workbook also includes:

* Data-model documentation
* Table relationships
* DAX practice questions
* DAX function references
* Modeling instructions

---

# ⭐ Data Model

The dataset uses a **Star Schema**.

```text
                         ┌───────────────┐
                         │    DimDate    │
                         └───────┬───────┘
                                 │
                                 │ 1 : *
                                 │
┌─────────────────┐       ┌──────▼────────┐       ┌─────────────────┐
│   DimProduct    │──────►│   FactSales   │◄──────│  DimCustomer    │
└─────────────────┘       └──────┬────────┘       └─────────────────┘
                                 │
                                 │ 1 : *
                                 │
                         ┌───────▼───────┐
                         │    DimStore   │
                         └───────────────┘
```

### Relationships

Create the following relationships when using the dataset in Power BI:

| Dimension                  | Fact                     |
| -------------------------- | ------------------------ |
| `DimDate[DateKey]`         | `FactSales[DateKey]`     |
| `DimProduct[ProductKey]`   | `FactSales[ProductKey]`  |
| `DimCustomer[CustomerKey]` | `FactSales[CustomerKey]` |
| `DimStore[StoreKey]`       | `FactSales[StoreKey]`    |

Recommended relationship configuration:

* **Cardinality:** One-to-Many (`1:*`)
* **Cross-filter direction:** Single
* **Dimension tables:** One side
* **Fact table:** Many side

---

# 📋 Dataset Tables

## 1. `FactSales`

The central fact table containing individual sales transactions.

Typical fields include:

* `SaleID`
* `DateKey`
* `ProductKey`
* `CustomerKey`
* `StoreKey`
* `Quantity`
* `UnitPrice`
* `Discount`
* `SalesAmount`
* `CostAmount`

This table contains the measurable business events used for analysis.

---

## 2. `DimDate`

Calendar dimension used for time-based analysis.

Includes fields such as:

* `DateKey`
* `Date`
* `Year`
* `Quarter`
* `Month`
* `MonthName`
* `Week`
* `DayOfWeek`

Use this table when practicing time-based analysis and DAX time-intelligence calculations.

---

## 3. `DimProduct`

Contains product-related information.

Includes attributes such as:

* `ProductKey`
* `ProductName`
* `Category`
* `SubCategory`
* `Brand`

Useful for analyzing product, category, subcategory, and brand performance.

---

## 4. `DimCustomer`

Contains customer information.

Includes attributes such as:

* `CustomerKey`
* `CustomerName`
* `Gender`
* `Age`
* `City`
* `State`
* `CustomerSegment`

Useful for customer segmentation and customer-level analysis.

---

## 5. `DimStore`

Contains store and geographic information.

Includes attributes such as:

* `StoreKey`
* `StoreName`
* `City`
* `State`
* `Region`

Useful for store, regional, and geographic performance analysis.

---

# 🧠 DAX Practice

The workbook contains **40+ DAX practice questions** organized from beginner to advanced.

## 🟢 Beginner

Practice fundamental aggregation functions such as:

```text
SUM
COUNT
COUNTROWS
AVERAGE
MIN
MAX
DISTINCTCOUNT
```

Example questions:

* What is the total sales amount?
* What is the total quantity sold?
* How many sales transactions are there?
* What is the average sales amount?
* How many unique customers are there?

---

## 🟡 Intermediate

Practice filter manipulation, iterators, relationships, and context.

Functions include:

```text
CALCULATE
FILTER
VALUES
DISTINCT
ALL
ALLEXCEPT
REMOVEFILTERS
KEEPFILTERS
SUMX
AVERAGEX
RELATED
RELATEDTABLE
SELECTEDVALUE
```

Example questions:

* Calculate sales for a selected customer.
* Calculate sales for a specific product category.
* Calculate average sales per customer.
* Calculate sales while ignoring a product filter.
* Calculate sales by customer segment.

---

## 🔴 Advanced

Practice time intelligence, ranking, dynamic filtering, and advanced evaluation contexts.

Functions include:

```text
RANKX
TOPN
ALLSELECTED
DATEADD
SAMEPERIODLASTYEAR
TOTALYTD
DATESYTD
HASONEVALUE
ISFILTERED
```

Example questions:

* Rank products by total sales.
* Find the Top 5 customers by revenue.
* Calculate year-over-year sales growth.
* Calculate Year-to-Date sales.
* Compare current-year and previous-year sales.
* Calculate contribution percentage.
* Build dynamic ranking measures.

---

# 🛠️ Skills You Can Practice

### Power BI

* Data loading
* Data modeling
* Star schema
* Relationships
* Cardinality
* Cross-filter direction
* Report development
* Data visualization
* KPI development

### DAX

* Aggregations
* Measures
* Row context
* Filter context
* Context transition
* `CALCULATE`
* Iterator functions
* Filter manipulation
* Virtual tables
* Time intelligence
* Ranking
* Top-N analysis
* Dynamic calculations

### SQL

Use the dataset to practice:

* `SELECT`
* `WHERE`
* `GROUP BY`
* `HAVING`
* `ORDER BY`
* `JOIN`
* Subqueries
* CTEs
* Window functions
* Aggregations
* Date analysis
* Customer analysis
* Product analysis
* Ranking
* Top-N queries

### Python

Use the dataset with libraries such as:

* Pandas
* NumPy
* Matplotlib

Practice:

* Data loading
* Data cleaning
* Exploratory Data Analysis
* Aggregations
* Grouping
* Merging tables
* Time-series analysis
* Customer analysis
* Product analysis
* Visualization

### Excel

Practice:

* Pivot Tables
* Pivot Charts
* XLOOKUP
* SUMIFS / COUNTIFS
* IF / IFS
* Data validation
* Conditional formatting
* Dashboard creation
* Data analysis

---

# 🚀 How to Use

## Power BI

### 1. Download the workbook

Download:

```text
Power_BI_DAX_Practice_Dataset.xlsx
```

### 2. Open Power BI Desktop

Go to:

```text
Home → Get Data → Excel
```

### 3. Import the tables

Load:

```text
FactSales
DimDate
DimProduct
DimCustomer
DimStore
```

### 4. Build the data model

Create the relationships described in the **Data Model** section.

### 5. Start practicing

Open the `DAX_Practice` sheet and work through the questions from beginner to advanced.

Try solving each question yourself before checking documentation or other solutions.

---

# 🐍 Using the Dataset with Python

You can load the workbook using Pandas:

```python
import pandas as pd

file = "Power_BI_DAX_Practice_Dataset.xlsx"

fact_sales = pd.read_excel(file, sheet_name="FactSales")
dim_product = pd.read_excel(file, sheet_name="DimProduct")
dim_customer = pd.read_excel(file, sheet_name="DimCustomer")
dim_store = pd.read_excel(file, sheet_name="DimStore")
dim_date = pd.read_excel(file, sheet_name="DimDate")
```

You can then combine the tables using `merge()` and perform exploratory analysis.

---

# 🗄️ Using the Dataset with SQL

Import the Excel tables into a SQL database such as **SQL Server**, PostgreSQL, MySQL, or another relational database.

Once the tables are imported, you can practice SQL queries using the relationships between the fact and dimension tables.

For example:

```sql
SELECT
    p.Category,
    SUM(f.SalesAmount) AS TotalSales
FROM FactSales f
JOIN DimProduct p
    ON f.ProductKey = p.ProductKey
GROUP BY p.Category
ORDER BY TotalSales DESC;
```

This allows you to practice SQL using the same relational structure used in Power BI.

---

# 📊 Suggested Learning Path

Follow this progression if you're using the dataset to build your data-analysis skills:

```text
1. Explore the Data
        ↓
2. Understand the Tables
        ↓
3. Understand Primary & Foreign Keys
        ↓
4. Build the Star Schema
        ↓
5. Practice SQL Queries
        ↓
6. Practice Excel Analysis
        ↓
7. Load Data into Power BI
        ↓
8. Create Relationships
        ↓
9. Learn Basic DAX
        ↓
10. Understand Filter & Row Context
        ↓
11. Learn CALCULATE
        ↓
12. Practice Iterators
        ↓
13. Learn Time Intelligence
        ↓
14. Practice Ranking & TOPN
        ↓
15. Build a Power BI Dashboard
```

---

# 💼 Portfolio Project Ideas

Once you are comfortable with the dataset, use it to build complete analytics projects.

### 1. Sales Performance Dashboard

Build an executive dashboard containing:

* Total Sales
* Total Profit
* Total Orders
* Total Customers
* Average Order Value
* YoY Growth
* Monthly Sales Trend

### 2. Product Analysis

Analyze:

* Top Products
* Product Ranking
* Category Performance
* Subcategory Performance
* Brand Performance

### 3. Customer Analysis

Analyze:

* Customer Segments
* Top Customers
* Customer Contribution %
* Sales by City
* Sales by State
* Customer-level purchasing behavior

### 4. Regional & Store Analysis

Analyze:

* Sales by Region
* Sales by State
* Store Performance
* Regional Trends
* Top-performing Stores

### 5. SQL Analytics Project

Create a collection of SQL queries covering:

* Business KPIs
* Customer analysis
* Product performance
* Monthly trends
* Top-N analysis
* Ranking
* Year-over-year comparisons

### 6. Python EDA Project

Perform an end-to-end exploratory analysis covering:

```text
Data Loading
    ↓
Data Cleaning
    ↓
Data Exploration
    ↓
Data Transformation
    ↓
Business Analysis
    ↓
Visualization
    ↓
Insights
```

---

# 🎓 Who Is This Dataset For?

This dataset is suitable for:

* Aspiring Data Analysts
* Data Analysts
* BI Developers
* Power BI Developers
* Business Intelligence professionals
* Students learning data analytics
* Professionals preparing for interviews
* Anyone practicing SQL, Python, Excel, Power BI, or DAX

---

# ⚠️ Dataset Disclaimer

This is a **synthetic dataset created for educational and practice purposes**.

It does not contain real customer information or confidential business data.

The data should not be interpreted as representing any actual company, customer, product, store, or transaction.

---

# 📜 License

This project is released under the **MIT License**.

See the [`LICENSE`](LICENSE) file for the complete license terms.

---

# ⭐ Support the Project

If you find this dataset useful for learning or practicing data analytics, consider giving the repository a ⭐.

You are welcome to use it for:

* Learning
* Practice
* Portfolio projects
* Interview preparation
* SQL projects
* Python projects
* Excel projects
* Power BI projects
* DAX experimentation

---

### 📌 Practice. Analyze. Build. Improve.

Use the same dataset across **Excel, SQL, Python, and Power BI** to strengthen your end-to-end data analytics skills.
