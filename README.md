# 📊 US Sales Performance Dashboard — Power BI

## 📌 Project Overview

An interactive **Power BI sales performance dashboard** built to transform transactional order data into clear, actionable business insights.

The dashboard analyzes **sales, profit, products, categories, sub-categories, and regional performance** across the United States. Interactive filters allow users to explore performance by **Region, Category, Sub-category, State, City, and Ship Date**.

The project demonstrates an end-to-end Power BI workflow: **data preparation → data modeling → DAX measures → interactive visualization → business insights**.

---

## 🖼️ Dashboard Preview

<img width="1435" height="808" alt="image" src="https://github.com/user-attachments/assets/3c68d32e-f4b7-4ee0-9465-e94ca3cfc879" />

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

## 👨‍💻 Author

**Bhavin Vaidya**
