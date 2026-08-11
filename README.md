# 📊 US Sales Performance Dashboard — Power BI

## 📌 Project Overview

An interactive **Power BI sales performance dashboard** built to transform transactional order data into clear, actionable business insights.

The dashboard analyzes **sales, profit, products, categories, sub-categories, and regional performance** across the United States. Interactive filters allow users to explore performance by **Region, Category, Sub-category, State, City, and Ship Date**.

The project demonstrates an end-to-end Power BI workflow: **data preparation → data modeling → DAX measures → interactive visualization → business insights**.

---

## 🖼️ Dashboard Preview

![US Sales Performance Dashboard](dashboard.png)

> **Note:** Add the dashboard screenshot to the repository and name it `dashboard.png` for the preview above to display correctly.

---

## 🛠️ Tech Stack & Skills

- **Tool:** Microsoft Power BI Desktop
- **Data Source:** Excel transactional order dataset (`Orders_data.xlsx`)
- **Data Transformation:** Power Query
- **Data Modeling:** Power BI data model / dimensional modeling concepts
- **Calculations:** DAX measures and aggregation functions
- **Visualization:** KPI Cards, Pie/Donut Charts, Bar Charts, Map Visualization, Slicers
- **Skills Demonstrated:**
  - Data cleaning and transformation
  - Data modeling
  - DAX
  - KPI development
  - Interactive report design
  - Geographic analysis
  - Product and category analysis
  - Business storytelling

---

## 📁 Dataset Overview

The dataset contains **9,994 transactional records** and **21 columns**.

Key fields include:

| Field | Description |
|---|---|
| `order_id` | Unique order identifier |
| `order_date` | Date the order was placed |
| `ship_date` | Date the order was shipped |
| `customer_id` | Customer identifier |
| `customer_name` | Customer name |
| `segment` | Customer segment |
| `region` | Sales region |
| `state` | Customer/order state |
| `city` | Customer/order city |
| `category` | Product category |
| `sub_category` | Product sub-category |
| `product_name` | Product name |
| `sales` | Sales/revenue amount |
| `quantity` | Quantity sold |
| `discount` | Discount applied |
| `profit` | Profit generated |

### Data Coverage

- **Orders:** 9,994 rows
- **Order Date:** January 2019 – December 2022
- **Ship Date:** January 2019 – January 2023
- **Regions:** West, East, Central, South
- **Categories:** Technology, Furniture, Office Supplies

---

## 📊 Dashboard KPIs

The dashboard provides six high-level KPIs:

| KPI | Value |
|---|---:|
| **Total Sales** | **$2.30M** |
| **Total Profit** | **$286.40K** |
| **Maximum Sale** | **$22.64K** |
| **Maximum Profit** | **$8.40K** |
| **Average Sale** | **$229.86** |
| **Number of Sales Records** | **9,994** |

These KPIs provide a quick overview of the overall health and scale of the business.

---

## 📈 Key Dashboard Features

### 1. 🌎 Regional Sales Analysis

A regional breakdown allows stakeholders to compare sales performance across:

- West
- East
- Central
- South

Based on the dataset:

- **West:** ~$725.46K
- **East:** ~$678.78K
- **Central:** ~$501.24K
- **South:** ~$391.72K

The **West region is the largest contributor to sales**, while the South represents the smallest of the four regions.

---

### 2. 🏷️ Category Performance

Sales are analyzed across three major product categories:

- **Technology:** ~$836.15K
- **Furniture:** ~$742.00K
- **Office Supplies:** ~$719.05K

Technology generates the highest total sales among the three categories.

---

### 3. 📦 Top 5 Sub-Categories by Sales

The dashboard highlights the highest-performing sub-categories:

1. **Phones** — ~$330.01K
2. **Chairs** — ~$328.45K
3. **Storage** — ~$223.84K
4. **Tables** — ~$206.97K
5. **Binders** — ~$203.41K

This visualization helps identify the products driving the largest share of revenue.

---

### 4. 💰 Top 5 Sub-Categories by Profit

The dashboard also separates **revenue performance from profitability**.

Top profitable sub-categories include:

1. **Copiers** — ~$55.62K
2. **Phones** — ~$44.52K
3. **Accessories** — ~$41.94K
4. **Paper** — ~$34.05K
5. **Binders** — ~$30.22K

This comparison demonstrates why analyzing **profit in addition to sales** is important. A product can generate high revenue without necessarily being the most profitable.

---

### 5. 🗺️ Geographic Analysis

The geographic visualization allows users to explore sales performance across the United States by location.

Users can combine geographic analysis with the dashboard filters to investigate:

- High-performing states
- Regional sales concentration
- City-level performance
- Geographic sales patterns

---

## 🎛️ Interactive Filters

The report includes slicers for:

- **Region**
- **Category**
- **Sub-category**
- **State**
- **City**
- **Ship Date**

These filters allow users to move from a high-level business overview to more detailed analysis.

---

## 🧮 DAX & Measures

The dashboard uses aggregation-based measures to calculate important business metrics.

Example measures include:

```DAX
Total Sales =
SUM(Orders[sales])
```

```DAX
Total Profit =
SUM(Orders[profit])
```

```DAX
Average Sales =
AVERAGE(Orders[sales])
```

```DAX
Maximum Sales =
MAX(Orders[sales])
```

```DAX
Maximum Profit =
MAX(Orders[profit])
```

```DAX
Count of Sales =
COUNTROWS(Orders)
```

These measures are then reused across multiple visuals so that the report remains dynamic when users apply slicers.

---

## 🔄 Data Preparation

Power Query can be used to prepare the transactional data before analysis, including:

- Checking and correcting data types
- Handling missing values
- Validating date fields
- Reviewing duplicate records
- Ensuring numerical fields are correctly formatted
- Preparing categorical fields for analysis
- Loading clean data into the Power BI model

The source dataset contains **11 missing postal-code values**, while the main analytical fields are populated.

---

## 🧩 Data Modeling

The project is designed around analytical reporting principles.

The primary transactional table contains:

- Orders
- Customers
- Products
- Geography
- Dates
- Sales
- Quantity
- Discount
- Profit

For a production-ready implementation, the model can be extended into a **star schema** with dedicated dimension tables such as:

```text
             DimCustomer
                  |
                  |
DimProduct ---- FactSales ---- DimDate
                  |
                  |
              DimGeography
```

This approach improves model organization, DAX readability, scalability, and reporting performance.

---

## 💡 Business Insights

The dashboard reveals several useful business insights:

- **Technology is the highest-selling category**, generating approximately $836K in sales.
- **The West region leads regional sales** at approximately $725K.
- **Phones and Chairs are the two largest sales-driving sub-categories**, each generating more than $328K.
- **Copiers generate the highest profit** among the major sub-categories, despite not being the highest-sales sub-category.
- Sales and profitability should be analyzed together because **high revenue does not automatically mean high profit**.
- Geographic and category filters allow stakeholders to identify where products are performing best and where additional investigation may be required.

---

## 🎯 Business Questions Answered

This dashboard is designed to answer questions such as:

- What are our total sales and profit?
- Which region generates the most sales?
- Which product category performs best?
- Which sub-categories generate the most revenue?
- Which sub-categories are the most profitable?
- Where are sales concentrated geographically?
- How does performance change when filtering by region, category, state, or city?
- Which products should management investigate for revenue or profitability opportunities?

---

## 📁 How to View the Project

1. Download the `.pbix` file from this repository.
2. Open the file using **Power BI Desktop**.
3. If the source file is not embedded, place `Orders_data.xlsx` in the expected location or update the data source path in Power Query.
4. Use the slicers to interact with the dashboard.
5. Explore the KPIs, regional analysis, category performance, and sub-category profitability.

### Repository Structure

```text
📁 PowerBI-Sales-Dashboard
│
├── 📊 Sales_Performance_Dashboard.pbix
├── 📄 Orders_data.xlsx
├── 🖼️ dashboard.png
└── 📖 README.md
```

---

## 🚀 Future Improvements

Potential enhancements for a more advanced version of the dashboard:

- Add **Year-over-Year (YoY) Sales Growth**
- Add **Profit Margin %**
- Add **Sales and Profit trend analysis over time**
- Add **Top/Bottom 10 products**
- Add **Customer segmentation analysis**
- Add **dynamic titles**
- Add **drill-through pages**
- Add **tooltips and bookmarks**
- Implement **Row-Level Security (RLS)**
- Optimize the model using a full **star schema**
- Add a dedicated **Date dimension**
- Add advanced **DAX time-intelligence measures**

---

## 📚 PL-300 Skills Demonstrated

This project supports preparation for the **Microsoft Power BI Data Analyst (PL-300)** certification by demonstrating:

- ✅ Prepare data
- ✅ Transform data using Power Query
- ✅ Understand data modeling
- ✅ Create DAX measures
- ✅ Use aggregation functions
- ✅ Build interactive visualizations
- ✅ Apply filters and slicers
- ✅ Analyze data geographically
- ✅ Communicate insights through dashboards
- ✅ Apply data storytelling principles

---

## 👨‍💻 Author

**Bhavin**

Aspiring Data Analyst | Power BI | SQL | Python | Data Analytics

This project is part of my journey toward transitioning into a **Data Analyst / Business Analyst** role and building a practical portfolio of end-to-end analytics projects.
