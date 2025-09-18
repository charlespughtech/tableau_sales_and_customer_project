# 📊 Tableau Sales and Customer Dashboards Project
#### Building interactive dashboards to analyse sales performance and customer insights using Tableau.

---

#### Project Repository URL: [charlespughtech/tableau_sales_and_customer_project](https://github.com/charlespughtech/tableau_sales_and_customer_project)

---

**Author:** Charles Pugh - Google-certified Data Analyst  
**Website:** [https://charlespughtech.github.io/](https://charlespughtech.github.io/)  
**Email:** [charlespughtech@gmail.com](mailto:charlespughtech@gmail.com)  
**LinkedIn:** [https://www.linkedin.com/in/charlespughtech/](https://www.linkedin.com/in/charlespughtech/)  
**Date:** 2025-09-18

---

Welcome to my **Tableau Sales and Customer Dashboards Project** repository!

View the interactive dashboards on [Tableau Public](https://public.tableau.com/app/profile/charlespughtech/viz/tableau_sales_project/SalesDashboard).

(**Note: not optimised for mobile devices**)

<a href="https://public.tableau.com/app/profile/charlespughtech/viz/tableau_sales_project/SalesDashboard">
<img width="1174" height="872" alt="Sales Dashboard" src="https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/sales_dashboard.jpg" />
</a>

<a href="https://public.tableau.com/app/profile/charlespughtech/viz/tableau_sales_project/SalesDashboard">
<img width="1174" height="872" alt="Customer Dashboard" src="https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/customer_dashboard.jpg" />
</a>

## 📖 Project Overview

**This project involves:**
- **Dashboard Creation:** Developing two interactive Tableau dashboards following a structured design process: analysing user story requirements, collecting specifications, choosing appropriate charts, drawing mockups, and selecting colours for the Sales Performance and Customer Analysis dashboards.
- **Visualisations:** KPI overviews with text tables, monthly and weekly trend line charts, product subcategory comparison bar charts, sales by category pie charts, and geographic maps to support data-driven decisions for sales managers and executives.
- **Data Integration:** Combining multiple CSV datasets to create a unified data model for analysis, with relationships established via Order ID and Postal Code.

---

## 🗃️ Data Architecture

This project uses four CSV datasets representing orders, customers, locations, and products. Relationships are established in Tableau to link data via Order ID (Orders to Customers and Products) and Postal Code (Orders to Location) for a seamless data model.
- **Datasets:** [Orders.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/non-eu/Orders.csv) (sales transactions), [Customers.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/non-eu/Customers.csv) (customer details), [Location.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/non-eu/Location.csv) (geographic data), [Products.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/non-eu/Products.csv) (product information).
- Data is available in both EU and non-EU number formats; non-EU version used for this project.
- Download datasets from [DataWithBaraa](https://www.datawithbaraa.com/tableau/tableau-sales-project-thank-you/).

---

## 🛠️ Important Links & Tools (Free)

- [**Datasets**](https://www.datawithbaraa.com/tableau/tableau-sales-project-thank-you/): Project datasets (CSV files in EU and non-EU formats).
- [**Tableau Desktop/Public**](https://www.tableau.com/products/desktop): Visualisation tool (free Public version available).
- [**Git Repository**](https://github.com/charlespughtech/tableau_sales_and_customer_project): Project source code and files.
- [**Project Mockups**](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/mockup.pdf): Dashboard sketches.
- [**Project Phases**](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/project_phases.pdf): Step-by-step design process.
- [**Requirements**](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/Tableau_Project_Requirements.pdf): Detailed specifications.

---

## 📋 Project Requirements

### Sales Performance Dashboard
#### Objective
Present an overview of sales metrics and trends in order to analyse year-over-year sales performance and understand sales trends.

Specifications:
- **KPI Overview:** Display a summary of total sales, profits and quantity for the current year and the previous year using text table cards.
- **Sales Trends:** Present the data for each KPI on a monthly basis for both the current year and the previous year using dual-axis line charts; identify months with highest and lowest sales and make them easy to recognise with colour highlights.
- **Product Subcategory Comparison:** Compare sales performance by different product subcategories for the current year and the previous year using side-by-side bar charts; include a comparison of sales with profit via a combined bar and line chart.
- **Weekly Trends for Sales & Profit:** Present weekly sales and profit data for the current year using line charts; display the average weekly values as reference lines; highlight weeks that are above and below the average to draw attention to sales & profit performance using conditional formatting.

### Customer Analysis Dashboard
#### Objective
Provide insights into customer segmentation, loyalty, and geographic distribution to support targeted marketing and sales strategies.

Specifications:
- **Customer KPIs:** Total customers, segments, and regions displayed in text table cards.
- **Top Customers:** Ranking by sales and profit using horizontal bar charts.
- **Geographic Map:** Sales by region/state using filled maps with generated latitude/longitude.
- **Segment Analysis:** Trends and comparisons across customer segments using stacked bar charts and pie charts for breakdowns.

---

## 🔎 Tableau Techniques Used (Basic to Advanced)
- **Data Connections:** Imported four CSV files with custom delimiters (semicolon) and encodings (UTF-8 or Windows-1252); established inner joins and relationships between Orders (via Order ID to Customers and Products; Postal Code to Location) for a seamless, performant data model.
- **Data Cleaning:** Formatted dates using DATETRUNC and DATEPART for month/year/week hierarchies; cleaned numeric fields (e.g., Sales, Profit with £ currency formatting, handling commas as decimal separators in non-EU data); replaced nulls in Quantity/Discount with zeros; standardised text fields like Segment and Category using string functions; created hierarchies for drill-down (e.g., Year > Month > Week).
- **Calculated Fields:** Developed fields for Year-over-Year (YoY) growth using DATEDIFF and LOOKUP for previous value comparisons; monthly/weekly trends with DATETRUNC('month', [Order Date]) and DATETRUNC('week', [Order Date]); profit margins as [Profit]/[Sales]; dynamic KPIs with IF YEAR([Order Date]) = [Current Year Parameter] THEN SUM([Sales]) ELSE 0 END; highest/lowest month identification using RANK(SUM([Sales])) OVER (ORDER BY SUM([Sales]) DESC); above/below average flags with IF SUM([Sales]) > WINDOW_AVG(SUM([Sales])) THEN 'Above' ELSE 'Below' END.
- **Parameters:** Implemented a "Current Year" parameter (integer list: 2020-2023) with parameter actions to dynamically toggle between years for filtering trends and comparisons; used for YoY calculations and dynamic titles like "Sales Trends for " + STR([Current Year Parameter]).
- **Level of Detail (LOD) Expressions:** {FIXED [Sub-Category] : SUM([Sales])} for subcategory totals independent of view filters; {FIXED [Week Number] : AVG([Sales])} for weekly averages across the dataset; {FIXED [Region] : COUNT([Customer ID])} for region-level customer counts.
- **Sheet Building:** 
  - KPI cards as text tables with SUM aggregations, conditional colour formatting (green for positive growth, red for negative), and custom number formats (£ for currency).
  - Dual-axis line charts for monthly/weekly trends (Sales/Profit on separate axes, synchronised), with reference lines for averages and colour marks for high/low points.
  - Side-by-side bar charts for subcategory comparisons (stacked by year, with measure names on colour).
  - Combined axis charts (bar for sales, line for profit) for subcategory sales vs. profit.
  - Pie charts for sales by category breakdowns, using dual colour marks.
  - Filled maps for geographic sales distribution, auto-generated lat/long from Location data, with size by profit and colour by sales.
- **Dashboard Assembly:** Utilised vertical and horizontal containers for responsive layout (main vertical container with title horizontal, BAN horizontal for KPIs, and chart horizontals/verticals below); added navigation buttons using image objects (e.g., [Icon - Sales Dashboard(active).png](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/Icon%20-%20Sales%20Dashboard(active).png) for active states); dynamic titles with parameter substitution; global filters synced across sheets (e.g., year, region); dashboard actions for filter (on select for maps) and highlight (on hover for bars).
- **Dynamic Features:** Parameter actions linked to year dropdown for real-time updates; highlight actions on trend charts to emphasise selected periods; detailed tooltips with YoY percentages and rankings; responsive design with device-specific layouts (desktop, tablet, phone); colour palette selection for accessibility (blues for sales, greens for profit).

---

## 🗃️ Repository Structure

```bash
tableau_sales_and_customer_project/
│
├── datasets/                               # Project datasets (CSV files)
│   ├── eu/                                 # EU number format versions
│   │   ├── [Customers.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/eu/Customers.csv)
│   │   ├── [Location.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/eu/Location.csv)
│   │   ├── [Orders.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/eu/Orders.csv)
│   │   └── [Products.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/eu/Products.csv)
│   └── non-eu/                            # Non-EU number format versions (used in project)
│       ├── [Customers.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/non-eu/Customers.csv)
│       ├── [Location.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/non-eu/Location.csv)
│       ├── [Orders.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/non-eu/Orders.csv)
│       └── [Products.csv](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/datasets/non-eu/Products.csv)
│
├── images/                                # Dashboard images and icons
│   ├── [Icon - Customer Dashboard (active).png](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/Icon%20-%20Customer%20Dashboard%20(active).png)
│   ├── [Icon - Customer Dashboard.png](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/Icon%20-%20Customer%20Dashboard.png)
│   ├── [Icon - Filter Hidden.png](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/Icon%20-%20Filter%20Hidden.png)
│   ├── [Icon - Filter Shown.png](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/Icon%20-%20Filter%20Shown.png)
│   ├── [Icon - Logo.png](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/Icon%20-%20Logo.png)
│   ├── [Icon - Sales Dashboard(active).png](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/Icon%20-%20Sales%20Dashboard(active).png)
│   ├── [Icon - Sales Dashboard.png](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/Icon%20-%20Sales%20Dashboard.png)
│   ├── [sales_dashboard.jpg](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/sales_dashboard.jpg)
│   └── [customer_dashboard.jpg](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/customer_dashboard.jpg)
│
├── docs/                                  # Project documentation
│   ├── [mockup.pdf](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/mockup.pdf)                         # Dashboard sketches
│   ├── [project_phases.pdf](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/project_phases.pdf)                 # Design process steps
│   └── [Tableau_Project_Requirements.pdf](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/Tableau_Project_Requirements.pdf)   # Specifications
│
├── [tableau_sales_and_customer_project.twbx](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/tableau_sales_and_customer_project.twbx) # Packaged Tableau workbook
│
├── README.md                              # Project overview and instructions
└── LICENSE                                # License information
```

---

## © Licence

This project is licensed under the [MIT License](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/LICENSE). You are free to use, modify, and share this project with proper attribution.

---

🤝🏻 Credit to [DataWithBaraa](https://github.com/DataWithBaraa) for inspiration, guidance, mockups, and project phases.

---

## 📩 Contact

**For any enquiries or further information, please contact**:

**Charles Pugh** - Google-certified Data Analyst  
**Website:** [https://charlespughtech.github.io/](https://charlespughtech.github.io/)  
**Email:** [charlespughtech@gmail.com](mailto:charlespughtech@gmail.com)  
**LinkedIn:** [https://www.linkedin.com/in/charlespughtech/](https://www.linkedin.com/in/charlespughtech/)

---
