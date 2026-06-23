# 🚚 Supply Chain Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python) ![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green) ![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-orange) ![Matplotlib](https://img.shields.io/badge/Matplotlib-Plots-red) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter) ![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)

---

## 📌 Project Overview

This project performs an end-to-end Exploratory Data Analysis (EDA) on the **DataCo Supply Chain Dataset**, a real-world e-commerce logistics dataset. The goal is to uncover patterns in delivery performance, sales trends, product profitability, and regional logistics behavior — ultimately helping businesses reduce late deliveries and optimize supply chain operations.

---

## 🎯 Objectives

- Analyze delivery status distribution and identify late delivery patterns
- Investigate region-wise, customer segment-wise, and category-wise late delivery rates
- Understand the impact of shipping mode and payment type on delivery performance
- Track monthly order volume trends over time
- Identify top-performing products and categories by sales and profit
- Pinpoint cities with the highest order frequency and late delivery counts

---

## 📂 Repository Structure

```
Supply-Chain-Analysis/
│
├── Supply_Chain_Analysis.ipynb   # Main Jupyter Notebook with full EDA
├── dashboard/
│   └── supply_chain_dashboard.png  # Power BI Dashboard screenshot
└── README.md
```

---

## 📊 Dataset

**Source:** [DataCo Smart Supply Chain for Big Data Analysis – Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)

The dataset contains transactional supply chain records including order details, customer demographics, product categories, shipping modes, delivery statuses, and financial metrics.

**After cleaning, the following columns were retained:**

| Category | Key Columns |
|---|---|
| Customer Info | Customer City, Customer Country, Customer Segment |
| Order Info | Order Region, Order City, Order Status, order date |
| Product Info | Product Name, Category Name, Department Name |
| Shipping | Shipping Mode, Days for shipment (scheduled), Days for shipping (real) |
| Financials | Sales, Order Profit Per Order, Order Item Quantity |
| Target | Delivery Status, is_late (engineered) |

> **Note:** Columns dropped during cleaning include Customer Email, Customer Password, Product Image, Latitude/Longitude, and other PII/redundant fields.

---

## 🛠 Tools & Libraries

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Matplotlib | Static visualizations |
| Seaborn | Statistical charts |
| Jupyter Notebook | Interactive analysis environment |
| Power BI | Interactive dashboard |

---

## 🔍 Analysis Performed

### 1. Data Cleaning & Feature Engineering
- Dropped irrelevant and PII columns (21 columns removed)
- Created `is_late` binary flag: `1` if Delivery Status = "Late delivery", else `0`
- Engineered `Delay_ship_days` = Scheduled days − Actual shipping days
- Parsed `order date (DateOrders)` to extract `Order Year` and `Order Month`

### 2. Delivery Performance Analysis
- **Delivery Status Distribution** — Bar chart showing count of each delivery status
- **Region-wise Late Delivery %** — Ranked bar chart of late delivery rate by order region
- **Customer Segment-wise Late Delivery %** — Late delivery breakdown by Consumer, Corporate, Home Office
- **Category-wise Late Delivery %** — Late delivery rate across all product categories
- **Shipping Mode vs Late Deliveries** — Count of late deliveries by shipping mode
- **Payment Type vs Late Deliveries** — Late delivery counts segmented by payment method

### 3. Sales & Logistic Performance
- **Sales by Category** — Full-width bar chart across all product categories
- **Monthly Order Volume Trend** — Time-series line chart (year-month) showing order flow over the dataset period
- **Top 10 Products by Sales** — Horizontal bar chart of best-selling products
- **Top 10 Categories by Sales** — Revenue-ranked category comparison
- **Top 10 Categories by Average Profit** — Profitability per order by category
- **Top 10 Categories by Total Profit** — Cumulative profit leaders

### 4. Geographic Analysis
- **Top 10 Cities by Sales** — Revenue by city
- **Top 10 Cities by Order Frequency** — Most active order cities
- **Top 10 Cities with Most Late Deliveries** — Delivery problem hotspots

### 5. Product Demand
- **Top 10 Most Purchased Products** — Based on total order item quantity

---

## 📈 Dashboard

The Power BI dashboard provides an interactive summary of key supply chain KPIs including delivery status breakdown, regional performance, and sales trends.

---

## 💡 Key Insights

- A significant share of orders experience **late delivery**, with certain regions and shipping modes being disproportionately impacted.
- **Standard Class shipping** is associated with the highest volume of late deliveries.
- Specific **product categories** consistently show higher late delivery rates, suggesting upstream stocking or fulfilment issues.
- **Monthly order volume** shows clear seasonal trends with notable peaks, useful for demand planning.
- A small set of **cities and products** drive the majority of both revenue and delivery complaints, making them priority targets for operational improvement.

---

## ▶️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Supply-Chain-Analysis.git
   cd Supply-Chain-Analysis
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook Supply_Chain_Analysis.ipynb
   ```

4. Ensure `DataCoSupplyChainDataset.csv` is in the same directory (or update the file path in the notebook).

---


## 🙋 Author

**Kirana**
- GitHub: [@kirana-23](https://github.com/kirana-23)

---

## 📃 License

Dataset credit: [DataCo Supply Chain Dataset on Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis).
