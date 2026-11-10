
# BlueMart Retail Data Analytics & Executive Dashboard

### End-to-End Retail Sales, Profitability, Product Performance & Inventory Analysis

**Python | Pandas | NumPy | Matplotlib | Plotly | Dash | Data Analytics | Business Intelligence**

---

## Project Overview

This project presents an end-to-end **Retail Data Analytics and Business Intelligence solution** developed using Python.

The project analyzes BlueMart retail data to understand sales performance, profitability, product performance, store operations, sales channels and inventory conditions.

The analysis transforms retail transaction data into meaningful business insights and presents the results through a professional **Executive Retail Analytics Dashboard** designed for management-level decision-making.

The project covers the complete analytics process, from data inspection and cleaning to business analysis, visualization and executive reporting.

### Project Objective

The main objective is to answer:

**"What is happening in the retail business, which areas are performing well and what should management pay attention to?"**

The analysis focuses on:

- Understanding sales trends over time.
- Identifying the highest-performing product categories.
- Comparing sales and profitability across products.
- Evaluating store and city performance.
- Understanding revenue contribution from sales channels.
- Identifying high-selling products with comparatively low inventory.
- Examining inventory reorder levels.
- Detecting products with relatively high sales but low profit.
- Presenting business findings through an executive dashboard.

---

## Dataset Overview

The project uses four related BlueMart retail datasets.

| Dataset | Description | Records |
|---|---|---:|
| Sales | Retail sales transactions | 641,843 |
| Products | Product and SKU information | 200 |
| Stores | Store and location information | 50 |
| Inventory | Store-level inventory snapshots | 8,735 |

### 1. Sales Dataset — `bm_sales.csv`

Contains transaction-level retail sales information.

**Important columns:**
- `date` — Transaction date
- `store_id` — Store identifier
- `sku_id` — Product identifier
- `customer_id` — Customer identifier
- `quantity` — Units sold
- `unit_price` — Selling price per unit
- `total_value` — Transaction sales value
- `channel` — Sales channel
- `discount_pct` — Discount percentage

### 2. Product Dataset — `bm_skus.csv`

Contains product information used for category and profitability analysis.

**Important columns:**
- `sku_id`
- `sku_name`
- `category`
- `subcategory`
- `unit_price`
- `cost_price`
- `brand`

### 3. Store Dataset — `bm_stores.csv`

Provides information about retail store locations.

**Important columns:**
- `store_id`
- `store_name`
- `city`
- `store_type`
- `opening_date`

### 4. Inventory Dataset — `bm_inventory.csv`

Contains inventory information at the store and SKU level.

**Important columns:**
- `store_id`
- `sku_id`
- `stock_on_hand`
- `reorder_point`
- `safety_stock`
- `last_restock_date`
- `snapshot_date`

### Reporting Period

- **Sales Analysis:** January 2021 – October 2025
- **Inventory Snapshot:** October 31, 2025
- **Retail Stores:** 50
- **Products / SKUs:** 200
- **Cities:** Dubai, Abu Dhabi, and Sharjah

---

## Tools & Technologies

| Technology | Purpose |
|---|---|
| Python | Data analysis and application development |
| Pandas | Data cleaning, merging, grouping, and aggregation |
| NumPy | Numerical operations |
| Matplotlib | Business data visualizations |
| Jupyter Notebook | Data exploration and analysis |
| Plotly | Interactive business charts |
| Dash | Executive dashboard application |
| HTML & CSS | Dashboard design and responsive layout |

---

## Project Workflow

### Step 1: Data Understanding

Explored all retail datasets to understand their structure, available attributes, data types, and relationships.

The initial analysis included:

- Dataset dimensions
- Column information
- Descriptive statistics
- Missing-value identification
- Duplicate-record detection
- Validation of product and store identifiers

### Step 2: Data Cleaning & Preparation

Performed data quality checks to improve the reliability of the analysis.

Key activities included:

- Identifying missing customer IDs.
- Detecting 45 duplicate sales records.
- Removing duplicate sales transactions.
- Converting date columns into appropriate date formats.
- Checking product and store relationships.
- Validating data consistency.
- Preparing related sales, product, and store information for business analysis.

**Result:** The cleaned sales dataset contains **641,798 transactions** after removing 45 duplicate records.

Missing customer identifiers were identified during the quality assessment.

### Step 3: Data Integration

Combined relevant sales, product, and store information using their identifiers.

This allowed the analysis to compare:

- Sales by product category
- Product and subcategory profitability
- Sales by store
- Sales by city
- Revenue by sales channel

Inventory data was examined separately for stock-related analysis.

### Step 4: Business Performance Analysis

Performed five core business analyses and three additional ad hoc analyses focused on inventory and product profitability.

### Step 5: Executive Dashboard Development

Built an executive dashboard to communicate the final business findings through a clean, management-friendly interface.

---

## Key Business Analysis

The project addresses five important retail business questions.

### 1. Sales Performance Over Time

**Business Question:** How are sales changing over time?

Analyzed monthly sales to understand changes in retail revenue throughout the reporting period.

**Analysis:**
- Monthly sales aggregation
- Sales trend visualization
- Identification of changes in monthly performance

**Key Finding:**

Monthly sales fluctuate across the reporting period, showing repeated increases and decreases.

**Business Importance:**

Tracking monthly sales helps management understand how revenue performance changes over time.

### 2. Category Sales & Profitability

**Business Question:** Which product categories generate the highest sales and profit?

Calculated total sales and profit for each product category.

Profit was calculated using:

`Profit = Total Sales Value - (Cost Price × Quantity Sold)`

**Key Finding:**

**Electronics** generated the highest total sales and profit among the analyzed categories.

**Business Importance:**

Category-level analysis identifies major contributors to business revenue and profit.

### 3. Most Profitable Products

**Business Question:** Which products are the most profitable?

Analyzed total profit at the product subcategory level.

The analysis identified the top 10 profitable subcategories.

**Key Finding:**

**Batteries and Cables** were the leading subcategories in the profitability ranking.

**Business Importance:**

Understanding product profitability helps management identify which product groups contribute most to earnings.

### 4. Store & City Performance

**Business Question:** Which stores and cities perform best?

Compared total sales across retail stores and cities.

**Key Findings:**

- **Dubai** generated the highest sales among the three cities.
- **BlueMart Store 41** ranked highest in total store sales.
- Sales performance varied across retail locations.

**Business Importance:**

Location-level analysis provides visibility into performance differences across the store network.

### 5. Sales Channel Performance

**Business Question:** Which sales channel contributes the most revenue?

Compared sales across the available retail channels:

- Store
- Website
- Mobile App
- Amazon.ae
- Noon

**Key Finding:**

The **Store** channel generated the highest revenue among the five sales channels.

**Business Importance:**

Channel analysis helps management understand where retail sales are generated.

---

## Additional Business Insights — Ad Hoc Analysis

Three additional analyses were performed to investigate product performance and inventory conditions.

### 1. High-Selling Products With Comparatively Low Stock

**Business Question:** Which high-selling products have comparatively low stock?

Compared product sales quantities with inventory stock levels.

The notebook identifies combinations where:

- Overall SKU sales quantity is above the median.
- Store-level stock on hand is below the median.

**Key Finding:**

The analysis identified several product-store combinations with relatively high overall product sales and comparatively low stock levels.

Examples include SKU 1001 and SKU 1196 in selected stores.

**Business Importance:**

These combinations highlight inventory positions that may require management attention.

**Important:** This comparison uses SKU-wide sales quantities and individual store stock levels. It identifies relative inventory conditions, not confirmed stockouts.

### 2. Inventory Reorder Point Analysis

**Business Question:** Which products have stock below their reorder point?

Compared available stock with predefined reorder thresholds.

**Key Finding:**

**0 inventory records** were below their reorder points in the analyzed inventory snapshot.

**Business Importance:**

The result provides visibility into reorder threshold compliance as of October 31, 2025.

### 3. High-Sales, Low-Profit Products

**Business Question:** Which products generate relatively high sales but lower profit?

Compared product-level sales and profit.

Products were identified when:

- Total sales exceeded the product sales median.
- Total profit was below the product profit median.

**Key Finding:**

Eight products met these conditions.

Examples include:

- Grocery_Rice_1121
- Household_Paper Products_1028
- Personal Care_Soap_1156
- Grocery_Pasta_1196

**Business Importance:**

High sales do not always translate into equally strong profits.

Comparing revenue and profitability provides a more complete understanding of product performance.

---

## Executive Retail Analytics Dashboard

An interactive dashboard was developed using **Plotly Dash** to present the business findings to senior management.

The dashboard is designed to communicate the results of the analysis without exposing data-cleaning procedures, Python code, or technical notebook workflows.

### Dashboard Features

#### Executive KPI Overview

The dashboard displays verified business indicators:

- 641,798 cleaned sales transactions
- 50 retail stores
- 200 products / SKUs
- 3 cities
- 0 inventory records below reorder point

#### Executive Summary

Highlights the main business findings in simple, professional language.

#### Sales & Profitability Performance

Provides visualizations covering:

- Monthly sales trends
- Category sales and profit
- Profitable product subcategories
- Store performance
- City performance
- Sales channel contribution

#### Product Performance

Includes interactive comparisons for products identified as having high sales and comparatively low profit.

Features include:

- Product selection filters
- Sales comparisons
- Sales-versus-profit visualization
- Interactive chart tooltips
- Filter reset functionality

#### Inventory Performance

Provides visibility into selected product-store inventory records.

Includes:

- SKU selection
- Store filtering
- Stock-on-hand comparisons
- Reorder point comparisons
- Safety stock information
- Reset Filters functionality

#### Management Takeaways

Summarizes the most important business observations related to revenue, profitability, locations, sales channels, and inventory.

### Dashboard Design

The dashboard follows a modern business intelligence design approach, featuring:

- Clean executive interface
- Professional KPI cards
- Consistent typography
- Responsive layout
- Clear chart headings
- Interactive charts
- Minimal visual clutter
- Simple management-focused language

### Dashboard Data Scope

The dashboard uses actual findings and outputs available in the completed Jupyter Notebook.

Full-period sales charts are preserved from the notebook's analysis outputs.

Interactive product and inventory views use the exact records available in the notebook outputs.

Because the full underlying CSV datasets are not embedded in the dashboard, filtering is limited to the supported product and inventory views. The historical sales charts remain full-period views rather than recalculating under those filters.

This keeps the dashboard consistent with the original analysis without generating unsupported values.

---

## Project Structure

```text
Retail-Data-Analytics/
│
├── Dataset/
│   ├── bm_sales.csv
│   ├── bm_skus.csv
│   ├── bm_stores.csv
│   └── bm_inventory.csv
│
├── Retail.ipynb
│
├── app.py
│
├──requirements.txt
│
└── README.md
```

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Replace the placeholder URL with your GitHub repository URL.

### 2. Install Required Libraries

For the complete notebook and dashboard project:

```bash
pip install numpy pandas matplotlib seaborn jupyter dash plotly
```

### 3. Run the Jupyter Notebook

```bash
jupyter notebook
```

Open:

`Retail.ipynb`

Make sure the original datasets are available inside the `Dataset/` folder.

### 4. Launch the Executive Dashboard

```bash
python app.py
```

### 5. Open the Dashboard

Visit the following address in your browser:

**http://127.0.0.1:8050**

The dashboard runs locally using Plotly Dash.


---

## Key Business Findings

The analysis produced the following management-level insights:

| Business Area | Key Finding |
|---------------|-------------|
| Sales Trends | Monthly sales fluctuate throughout the reporting period. |
| Category Performance | Electronics leads in total sales and profit. |
| Product Profitability | Batteries and Cables lead the subcategory profit ranking. |
| City Performance | Dubai generates the highest sales. |
| Store Performance | BlueMart Store 41 leads total store sales. |
| Sales Channels | Physical stores contribute the highest channel revenue. |
| Inventory | No inventory records fall below the reorder point. |
| Product Sales vs Profit | Eight products have above-median sales but below-median profit. |

---

## Management Takeaways

Based on the completed analysis:

**1. Monitor Sales Performance**

Monthly sales change over time, making trend monitoring important for understanding revenue performance.

**2. Understand Major Revenue Contributors**

Electronics is the leading category in both sales and profit.

**3. Compare Retail Locations**

Dubai and BlueMart Store 41 lead their respective sales rankings, while performance differs across other locations.

**4. Monitor Sales Channel Contribution**

The Store channel is the largest individual revenue contributor.

**5. Review Product Profitability**

Some products generate relatively high revenue but lower profit, showing the importance of evaluating both measures together.

**6. Maintain Inventory Visibility**

No reorder-point breaches were found in the analyzed snapshot, although selected high-selling SKUs have comparatively low stock at certain stores.

---

## Skills Demonstrated

This project demonstrates practical skills in:

### Data Analytics
- Exploratory Data Analysis (EDA)
- Data cleaning and preparation
- Missing-value analysis
- Duplicate detection
- Data validation
- Dataset integration
- Data aggregation and grouping

### Business Analytics
- Retail sales analysis
- Profitability analysis
- Product performance evaluation
- Store and location analysis
- Sales channel analysis
- Inventory analysis
- KPI reporting
- Business insight generation

### Data Visualization & BI
- Data storytelling
- Business performance charts
- Interactive dashboards
- KPI visualization
- Executive reporting
- Management-focused dashboard design

### Python Development
- Pandas data manipulation
- NumPy operations
- Matplotlib and Seaborn visualization
- Plotly chart development
- Dash application development
- Interactive dashboard callbacks

---

## Project Outcome

Successfully completed an end-to-end retail analytics project covering **641,843 original sales records, 200 products, 50 stores and 8,735 inventory records**.

The project demonstrates how raw retail datasets can be transformed into actionable business information through:

1. Data quality assessment and cleaning.
2. Retail sales and profitability analysis.
3. Store, city, and channel performance evaluation.
4. Product and inventory analysis.
5. Business insight generation.
6. Executive dashboard development.

The final solution combines a detailed Python analytics notebook with a professional executive dashboard that presents key retail findings in a clear and accessible format.

---

## Author

**Aditya Sharma**

*Data Analytics | Python | SQL | Power BI | Business Intelligence*

**GitHub:** [Your GitHub Profile](https://github.com/YOUR-USERNAME)

**LinkedIn:** [Your LinkedIn Profile](https://www.linkedin.com/in/YOUR-PROFILE/)

---

### Project Summary

**Retail Data Analytics & Executive Dashboard** is a portfolio project showcasing the practical application of Python, data analysis, business intelligence and interactive visualization to understand retail performance and communicate data-driven insights.

The project demonstrates the complete journey from retail data to management-level business reporting.

**If you find this project useful, consider giving the repository a star! ⭐**
