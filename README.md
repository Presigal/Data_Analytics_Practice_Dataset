# 📊 Power BI & DAX Practice Dataset

A realistic **Power BI and DAX practice dataset** designed for Data Analysts, BI Developers, Power BI learners, and anyone preparing for Power BI/DAX interviews.

This project provides a complete **star-schema sales dataset** along with DAX practice questions covering everything from basic aggregations to advanced filter context, time intelligence, ranking, and virtual-table concepts.

---

## 🎯 Project Objective

The goal of this project is to provide a realistic dataset for practicing:

* Power BI data modeling
* Star schema design
* DAX fundamentals
* Filter context and row context
* `CALCULATE()`
* Iterator functions
* Time intelligence
* Ranking and Top N analysis
* Customer and product analysis
* KPI calculations
* Virtual tables
* Advanced DAX concepts

---

## 📦 What's Included

The Excel workbook contains **5 tables**:

| Table         | Description                  |
| ------------- | ---------------------------- |
| `FactSales`   | Sales transaction fact table |
| `DimDate`     | Date/calendar dimension      |
| `DimProduct`  | Product information          |
| `DimCustomer` | Customer information         |
| `DimStore`    | Store information            |

The workbook also contains:

* Schema/relationship documentation
* DAX practice questions
* DAX function reference
* Data-modeling instructions

---

## ⭐ Data Model

The dataset follows a **Star Schema**:

```text
                    ┌───────────────┐
                    │    DimDate    │
                    └───────┬───────┘
                            │
                            │ 1 : *
                            │
┌─────────────────┐   ┌─────▼─────────┐   ┌─────────────────┐
│   DimProduct    │───│   FactSales   │───│  DimCustomer    │
└─────────────────┘   └─────▲─────────┘   └─────────────────┘
                            │
                            │ 1 : *
                            │
                    ┌───────┴───────┐
                    │    DimStore   │
                    └───────────────┘
```

### Relationships

Create the following relationships in Power BI:

```text
DimDate[DateKey]       → FactSales[DateKey]
DimProduct[ProductKey] → FactSales[ProductKey]
DimCustomer[CustomerKey] → FactSales[CustomerKey]
DimStore[StoreKey]     → FactSales[StoreKey]
```

All relationships should be:

* **Cardinality:** One-to-Many (`1:*`)
* **Cross-filter direction:** Single
* **Dimension:** One side
* **Fact:** Many side

---

# 📋 Tables

## 1. FactSales

Contains individual sales transactions.

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

This is the main **fact table** containing measurable business events.

---

## 2. DimDate

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

Use this table for DAX time-intelligence calculations rather than directly using dates from the fact table.

---

## 3. DimProduct

Contains product-related information.

Includes attributes such as:

* `ProductKey`
* `ProductName`
* `Category`
* `SubCategory`
* `Brand`

Useful for practicing product-level analysis and hierarchical reporting.

---

## 4. DimCustomer

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

## 5. DimStore

Contains store information.

Includes attributes such as:

* `StoreKey`
* `StoreName`
* `City`
* `State`
* `Region`

Useful for regional and store-performance analysis.

---

# 🧠 DAX Practice

The workbook includes progressively difficult DAX questions.

### 🟢 Beginner

Practice functions such as:

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

### 🟡 Intermediate

Practice:

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
* Calculate sales ignoring the product filter.
* Calculate sales for each customer segment.

---

### 🔴 Advanced

Practice:

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
* Compare current-year sales with previous-year sales.
* Calculate sales percentage of the selected total.
* Build dynamic ranking measures.

---

# 🛠️ Skills Practiced

This project helps you practice:

### Power BI

* Data loading
* Data modeling
* Star schema
* Relationships
* Cardinality
* Filter direction
* Report building
* Data visualization

### DAX

* Aggregations
* Iterators
* Filter context
* Row context
* Context transition
* `CALCULATE`
* Virtual tables
* Time intelligence
* Ranking
* Top N analysis
* Dynamic calculations

### Data Analytics

* Sales analysis
* Customer analysis
* Product analysis
* Store analysis
* Regional analysis
* KPI analysis
* Trend analysis

---

# 🚀 How to Use

### Step 1 — Download the Dataset

Download:

```text
Power_BI_DAX_Practice_Dataset.xlsx
```

from this repository.

### Step 2 — Open Power BI Desktop

Open **Power BI Desktop** and select:

```text
Home → Get Data → Excel
```

### Step 3 — Load the Tables

Import the following tables:

```text
FactSales
DimDate
DimProduct
DimCustomer
DimStore
```

### Step 4 — Create Relationships

Create the relationships described in the **Data Model** section.

### Step 5 — Start Practicing DAX

Open the `DAX_Practice` sheet in the workbook and work through the questions from beginner to advanced.

Try to solve the questions **without looking up the answer first**.

---

# 📈 Suggested Learning Path

A recommended progression is:

```text
1. Import Data
       ↓
2. Understand Tables
       ↓
3. Build Star Schema
       ↓
4. Create Relationships
       ↓
5. Learn Basic DAX
       ↓
6. Learn CALCULATE
       ↓
7. Understand Filter Context
       ↓
8. Learn Iterators
       ↓
9. Learn Time Intelligence
       ↓
10. Learn Ranking & TOPN
       ↓
11. Practice Advanced DAX
       ↓
12. Build a Power BI Dashboard
```

---

# 💼 Recommended Portfolio Project

After completing the DAX exercises, use the same dataset to build a complete **Sales Performance Dashboard**.

Suggested dashboard sections:

### Executive Overview

* Total Sales
* Total Profit
* Total Orders
* Total Customers
* Average Order Value
* YoY Growth

### Sales Analysis

* Monthly sales trend
* Sales by category
* Sales by brand
* Sales by region

### Customer Analysis

* Top customers
* Customer segments
* Sales by city/state
* Customer contribution %

### Product Analysis

* Top 10 products
* Product ranking
* Category performance
* Subcategory performance

---

# 👨‍💻 Who Is This For?

This dataset is suitable for:

* Aspiring Data Analysts
* Data Analysts
* BI Developers
* Power BI Developers
* Business Intelligence professionals
* Students learning Power BI
* Professionals preparing for interviews
* Anyone learning DAX

---

# ⭐ If This Helps You

If you find this dataset useful for learning Power BI or DAX, consider giving the repository a ⭐.

Feel free to use the dataset for:

* Learning
* Practice
* Portfolio projects
* Interview preparation
* DAX experimentation

---

## 📜 License

This project is intended for educational and practice purposes.

See the [`LICENSE`](LICENSE) file for usage terms.
