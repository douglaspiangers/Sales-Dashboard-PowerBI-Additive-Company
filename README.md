# Sales Dashboard — Additives & Lubricants

An interactive sales dashboard built with **Power BI** for a Brazilian company in the additives and lubricants sector, covering **2023 to 2025**.

---

## Live Dashboard

[![Sales Dashboard Preview](assets/screenshots/dashboard_preview.png)](https://app.powerbi.com/view?r=eyJrIjoiNDFiN2RjNzgtNzllYi00MTBiLWE5ZDktOWU2YzU2M2QzMjc0IiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)

> **[Access the Published Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNDFiN2RjNzgtNzllYi00MTBiLWE5ZDktOWU2YzU2M2QzMjc0IiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)**

---

## About

This project transforms a raw sales spreadsheet into an interactive analytical dashboard. The goal is to provide visibility into the company's commercial performance, with intuitive navigation, drill-through for detailed analysis, and a custom visual identity.

---

## Tech Stack

| Tool              | Purpose                                       |
|-------------------|-----------------------------------------------|
| Power BI Desktop  | Data modeling, DAX measures, visuals, design  |
| Microsoft Excel   | Raw data source (Sales_2023_2025)             |
| Power Query       | ETL and data transformation                   |

---

## Repository Structure

```
sales-dashboard-powerbi/
├── data/
│   └── Sales_2023_2025.xlsx       # Raw sales data
├── assets/
│   └── screenshots/               # Dashboard screenshots
├── salesdashboard.pbix            # Power BI Desktop file
└── README.md
```

---

## Development Process

### Step 1 — Data Import
- Data imported from **Microsoft Excel** (`data/Sales_2023_2025.xlsx`)
- Connected via Power Query Editor for initial load and transformation

### Step 2 — First Charts and Visuals
- Created initial exploratory visuals to understand data distribution
- Identified key business metrics: revenue, volume, and customers

### Step 3 — Data Types & Headers Cleanup
- Fixed incorrect data types: text fields misclassified as numbers and vice versa
- Standardized column headers and naming conventions
- Cleaned null values and source inconsistencies

### Step 4 — Custom Design
- Created a custom visual theme aligned with the company's identity
- Defined color palette, standardized fonts, and layout organized by information hierarchy

### Step 5 — DAX Measures & Organization
- Built DAX measures for main KPIs (revenue, average ticket, YoY variance, etc.)
- Organized all measures in a dedicated **measures table** (`_Measures`), separate from data tables
- This structure avoids implicit measures and enables reuse across other reports

### Step 6 — Measures Table
- Created a central measures table for DAX governance and organization
- Measures grouped by category (Sales, Customers, Comparisons)

### Step 7 — Dashboard Design Refinement
- Refined layout after measure creation
- Revised visual alignment, spacing, and information hierarchy

### Step 8 — Floating Navigation Menu
- Implemented a **floating navigation menu** with page buttons
- Significantly improved usability and page-switching experience

### Step 9 — Measure Value Formatting
- Formatted values: BRL (R$) for currency, % for percentages, thousand separators
- Abbreviated units (K, M) for large values on card visuals

### Step 10 — Drill-through
- Configured **drill-through** for detailed analysis by dimension
- Users can right-click any visual and access a detail page filtered by the selected context

### Step 11 — Icons & Custom Tooltip
- Added icons to enrich the visual identity and guide the user
- Created a **custom tooltip page** showing additional data on hover

### Step 12 — Publishing
- Dashboard published to **Power BI Service** with a public access link
- Embed available via iframe for portfolio and website integration

---

## Raw Data

The dataset covers 2023 to 2025 and includes:

- Sale date and period
- Products (additives and lubricants)
- Customers and regions
- Revenue and quantity figures

> The `Sales_2023_2025.xlsx` file is available in the `data/` folder for replication and audit.

---

## How to Open

1. Clone this repository:
   ```bash
   git clone https://github.com/douglaspiangers/sales-dashboard-powerbi.git
   ```
2. Open `salesdashboard.pbix` in **Power BI Desktop**
3. If needed, update the data source path to point to `data/Sales_2023_2025.xlsx`

---

## Author

**Douglas Mengue**  
Data Analyst | Power BI | SQL | Python  
[LinkedIn](https://linkedin.com/in/douglasmengue) · [GitHub](https://github.com/douglaspiangers)
