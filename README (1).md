# 📦 Amazon Sales Dashboard — Power BI

An interactive, multi-page Power BI dashboard analyzing Amazon sales data across products, regions, and operations. Built with advanced Power BI features including DAX measures, Power Query transformations, and dynamic navigation buttons.

---

## 🖥️ Dashboard Preview

| Overview | Product Performance |
|----------|-------------------|
| ![Overview](screenshots/overview.png) | ![Products](screenshots/products.png) |

| Region | Operations |
|--------|------------|
| ![Region](screenshots/region.png) | ![Operations](screenshots/operations.png) |

---

## 📊 Key Metrics (All-Time)

| Metric | Value |
|--------|-------|
| 💰 Total Sales | 2.30M |
| 📈 Total Profit | 286.40K |
| 🛒 Total Orders | 10K |
| 📉 Avg Profit Margin | 12.47% |

---

## 📑 Dashboard Pages

### 1. Overview
- Total Sales by Year (2014–2017)
- Total Sales by Month (seasonal trend)
- Quantity Sold by Year
- Avg Order Value by Year
- Order Date & Category slicers

### 2. Product Performance
- Total Sales by Category (Office Supplies, Furniture, Technology)
- Avg Profit Margin by Product Name
- Category-wise: Avg Order Value, Sum of Sales, Sum of Profit

### 3. Region
- Total Sales by City (bar chart)
- Sum of Profit by City
- Interactive map visual

### 4. Operations
- Count of Order-to-Ship Days by State
- Orders by Shipping Duration (donut chart — Over 3 Days vs Within 3 Days)
- Orders Over 3 Days by State
- Orders Within 3 Days by State

---

## 🛠️ Technical Features Used

- **Power Query** — Data cleaning, transformation, and merging multiple tables
- **Table Joins** — Relationships built across fact and dimension tables
- **DAX Measures** — Custom KPIs: Total Sales, Total Profit, Avg Profit Margin, Avg Order Value
- **New Columns** — Calculated columns using DAX (e.g., `DATEDIFF` for shipping duration)
- **Navigation Buttons** — Actionable buttons (Overview, Products, Region, Operations) for seamless page navigation
- **Slicers** — Order Date and Category filters applied across all pages
- **Custom Visuals** — Bar charts, line charts, donut charts, and map visuals

---

## 📐 DAX Highlights

```dax
-- Avg Profit Margin
Avg Profit Margin = AVERAGE('Orders'[Profit Margin])

-- Total Profit
Total Profit = SUM('Orders'[Profit])

-- Shipping Days
Shipping Days = DATEDIFF('Orders'[Order Date], 'Orders'[Ship Date], DAY)

-- Orders Over 3 Days
Orders Over 3 Days = CALCULATE(COUNTROWS('Orders'), 'Orders'[Shipping Days] > 3)
```

---

## 🗂️ Project Structure

```
amazon-sales-dashboard-powerbi/
│
├── amazon_sales_dashboard.pbix   # Main Power BI file
├── README.md
├── screenshots/
│   ├── overview.png
│   ├── products.png
│   ├── region.png
│   └── operations.png
└── data/
    └── amazon_sample_data.xlsx   # Source data (if shareable)
```

---

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/amazon-sales-dashboard-powerbi.git
   ```
2. **Open** `amazon_sales_dashboard.pbix` in Power BI Desktop
3. If prompted, update the data source path under **Transform Data → Data Source Settings**
4. Click **Refresh** to reload the data

---

## 💡 Insights & Findings

- 📌 **Sales peaked in 2017**, showing consistent year-over-year growth from 2014
- 📌 **Office Supplies** leads in order volume (6.03K orders), while **Technology** leads in avg order value (452.71)
- 📌 **New York City** and **Los Angeles** are the top-performing cities by both sales and profit
- 📌 **67.71%** of orders ship within 3 days; California has the highest count of delayed shipments
- 📌 Avg order value dipped in 2015–2016 but recovered in 2017 (235.49)

---

## 🧰 Tools & Technologies

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)

---

## 👤 Author

**Thanveer Abdul Gafoor**  
📧 [LinkedIn](https://linkedin.com/in/your-profile) | 🐙 [GitHub](https://github.com/your-username)

---

## ⭐ Show Your Support

If you found this project useful, please consider giving it a ⭐ on GitHub — it helps others discover it!
