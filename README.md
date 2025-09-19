# 📊 Tableau Sales & Customer Analytics Project

---

**Author:** Charles Pugh – Google-certified Data Analyst  
**Website:** [https://charlespughtech.github.io/](https://charlespughtech.github.io/)  
**Email:** [charlespughtech@gmail.com](mailto:charlespughtech@gmail.com)  
**LinkedIn:** [https://www.linkedin.com/in/charlespughtech/](https://www.linkedin.com/in/charlespughtech/)  
**Date:** 2025-09-19  

---

Welcome to my **Tableau Sales & Customer Analytics Project**!  

---

#### View the live dashboards and worksheets now on **Tableau Public:  
[Tableau Sales & Customer Dashboards Project](https://public.tableau.com/app/profile/charlespughtech/viz/tableau_sales_project/SalesDashboard)**

---

**Project Repository URL:**  
[charlespughtech/tableau_sales_and_customer_project](https://github.com/charlespughtech/tableau_sales_and_customer_project)

---

## 📖 Project Overview

This dashboard-driven project demonstrates a complete sales and customer analytics workflow in Tableau – from connecting and modelling data, through to dynamic dashboard delivery and business insight.

- Covers *end-to-end analytics*: data preparation, calculated fields, KPIs, dynamic visuals, user navigation, and reporting.
- Designed for clarity, interactivity, and modern dashboard best-practice.

---

## 🗂️ Project Navigation

- [Sales Dashboard on Tableau Public](https://public.tableau.com/app/profile/charlespughtech/viz/tableau_sales_project/SalesDashboard)
- [Dataset Download (non-EU)](https://github.com/charlespughtech/tableau_sales_and_customer_project/tree/main/datasets/non-eu/)
- [Dataset Download (EU)](https://github.com/charlespughtech/tableau_sales_and_customer_project/tree/main/datasets/eu/)
- [Requirements PDF](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/Tableau_Project_Requirements.pdf)
- [Project Phases PDF](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/project_phases.pdf) (credit: [DataWithBaraa](https://github.com/DataWithBaraa/))
- [Mockup PDF](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/mockup.pdf) (credit: [DataWithBaraa](https://github.com/DataWithBaraa/))
- [Images Folder](https://github.com/charlespughtech/tableau_sales_and_customer_project/tree/main/images/)
- [Project Tableau Workbook](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/tableau_sales_and_customer_project.twbx)

---

## 🌳 Repository Branch & Directory Layout

This project uses a **single `main` branch** structure for simplicity and transparency. All resources are stored within a clearly organised directory tree:

---

```bash

tableau_sales_and_customer_project/
├── datasets/
│ ├── eu/
│ │ ├── Customers.csv
│ │ ├── Orders.csv
│ │ ├── Products.csv
│ │ └── Location.csv
│ └── non-eu/
│ ├── Customers.csv
│ ├── Orders.csv
│ ├── Products.csv
│ └── Location.csv
├── docs/
│ ├── Tableau_Project_Requirements.pdf
│ ├── mockup.pdf
│ └── project_phases.pdf
├── images/
│ ├── Icon - Customer Dashboard (active).png
│ ├── Icon - Customer Dashboard.png
│ ├── Icon - Filter Hidden.png
│ ├── Icon - Filter Shown.png
│ ├── Icon - Logo.png
│ ├── Icon - Sales Dashboard(active).png
│ ├── Icon - Sales Dashboard.png
│ ├── sales_dashboard.jpg
│ └── customer_dashboard.jpg
├── LICENSE
├── README.md
└── tableau_sales_and_customer_project.twbx

```

---


- **`datasets/`** — Contains all .csv files (EU and non-EU formats) for immediate analysis.
- **`docs/`** — Holds all core project documentation PDFs (requirements, blueprints, phases).
- **`images/`** — Includes navigation icons, logos, and dashboard screenshots for branding and README embedding.
- **`tableau_sales_and_customer_project.twbx`** — The fully packaged Tableau workbook with all dashboards, calculated fields, and settings.
- **`LICENSE`** — Licensed under MIT for open sharing.
- **`README.md`** — Comprehensive project documentation (this file).

### 🔗 [Browse the repository directly on GitHub](https://github.com/charlespughtech/tableau_sales_and_customer_project/)

---

## 🏆 Key Features & Deliverables

- **Dynamic Dual Dashboards**  
  - *Sales Dashboard*: Trends in sales, profit, and quantity; subcategory and time-series breakdowns with KPIs, YoY comparisons, and minimum/maximum highlights.  
  - *Customer Dashboard*: Customer growth, sales per customer, orders trend, top customers and distribution – including tailored visuals for individual and summary analysis.

- **Modern Interactivity**  
  - Clickable navigation buttons (image-based, highlights active view)
  - Toggle filters with on-dashboard visual cues.
  - Parameter-driven analysis (dynamic year selectors, highlight toggles, and more).
  - Coordinated filters across sheets for seamless data exploration.

- **Advanced Tableau Skills Demonstrated**  
  - *Multi-table data model* using Customers, Orders, Products, Locations (joined in Tableau’s data pane).
  - *Calculated fields* built for KPIs, YoY change, percent-to-total, ranks, labels, dynamic titling, and custom highlights.
  - *Dual synchronised axes* for direct comparison (e.g. sales vs profit).
  - *Interactive tooltips* contextual to current selection.
  - *Dashboard actions*: navigation, highlight, and filter.
  - *Consistent branding* via custom icons and images for navigation/filter states.
  - *Clean, modular layouts* with modern UX considerations.

- **Comprehensive Documentation**  
  - Project phases and dashboard design mockups included ([see docs](https://github.com/charlespughtech/tableau_sales_and_customer_project/tree/main/docs/)), credited to [DataWithBaraa](https://github.com/DataWithBaraa/).
  - Complete requirements specification for full replicability.

- **Open Assets for Reproducibility**  
  - Downloadable datasets (EU and non-EU versions, ready for Tableau).
  - Full packaged Tableau workbook (`.twbx`) for local exploration or editing.

---

## 📊 Dashboard Samples

[![Sales Dashboard](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/sales_dashboard.jpg)](https://public.tableau.com/app/profile/charlespughtech/viz/tableau_sales_project/SalesDashboard)
[![Customer Dashboard](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/images/customer_dashboard.jpg)](https://public.tableau.com/app/profile/charlespughtech/viz/tableau_sales_project/SalesDashboard)

*Click the images to launch the interactive dashboards on Tableau Public.*

---

## 💡 Charts & Techniques Used

- KPI summary cards (Sales, Profit, Quantity, Customers, Orders, etc.)
- Time-series (dual axis line + area/shape charts)
- Subcategory vertical bar and highlight bar charts
- Histograms and distribution charts
- Top 10 ranked tables (with calculated rank and sorting)
- Customer order distribution (bar/frequency)
- Dynamic colour encoding by performance (YoY/change)
- Parameter-driven views and toggles (active/inactive navigation, filter show/hide)
- Responsive dashboard layout and mobile-friendly navigation

---

## 📝 How to Use

1. **Download datasets** ([non-EU](https://github.com/charlespughtech/tableau_sales_and_customer_project/tree/main/datasets/non-eu) or [EU](https://github.com/charlespughtech/tableau_sales_and_customer_project/tree/main/datasets/eu)).
2. Open the `tableau_sales_and_customer_project.twbx` file in Tableau Desktop or Tableau Public Desktop.
3. Use the navigation, controls, and filters in the dashboards to explore sales and customer insights interactively.
4. Review the [Tableau Project Requirements](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/Tableau_Project_Requirements.pdf), [mockup](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/mockup.pdf), and [project phases](https://github.com/charlespughtech/tableau_sales_and_customer_project/blob/main/docs/project_phases.pdf) for methodology and design details.

---

## 🙏 Credits

- Project mentorship, blueprints & mockups by [DataWithBaraa](https://github.com/DataWithBaraa) | [Original datasets and dashboard idea](https://www.datawithbaraa.com/tableau/tableau-sales-project-thank-you/)
- All analysis, dashboards, and README authored by Charles Pugh.

---

*For feedback, collab, or questions, reach out via [email](mailto:charlespughtech@gmail.com) or connect on [LinkedIn](https://www.linkedin.com/in/charlespughtech/).*
---
