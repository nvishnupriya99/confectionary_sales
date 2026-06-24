# 🍬 British Confectionary Sales Analysis

An end-to-end exploratory analysis and interactive dashboard for UK confectionary sales data, built with Python, Plotly, and Dash.

---

## Overview

This notebook analyses a multi-region UK confectionary sales dataset (`Confectionary [4564].xlsx`), covering revenue, profit margins, units sold, and seasonal trends across England, Scotland, Wales, Northern Ireland, and Jersey. It culminates in a live, filterable Dash dashboard.

---

## Requirements

Install dependencies before running:

```bash
pip install dash plotly pandas numpy seaborn matplotlib scipy openpyxl
```

Or install the two key packages the notebook installs inline:

```bash
pip install dash plotly
```

---

## Data

Place the following file in the **same directory** as the notebook before running:

```
Confectionary [4564].xlsx
```

**Expected columns:**

| Column | Description |
|---|---|
| `Date` | Sale date |
| `Country(UK)` | Region (England, Scotland, Wales, N. Ireland, Jersey) |
| `Confectionary` | Product type |
| `Units Sold` | Number of units sold |
| `Cost(£)` | Cost in GBP |
| `Revenue(£)` | Revenue in GBP |
| `Profit(£)` | Profit in GBP |

---

## Notebook Structure

**1 — Setup & Imports**
Loads all libraries: `pandas`, `numpy`, `seaborn`, `matplotlib`, `plotly`, `scipy`, and `dash`.

**2 — Data Loading & Inspection**
Reads the Excel file, inspects sheets, unique values, and data types.

**3 — Distribution Analysis**
Plots histograms with KDE for `Units Sold`, `Cost(£)`, `Profit(£)`, and `Revenue(£)`, and prints skewness for each.

**4 — Revenue Breakdown**
Summarises total revenue by country and product using grouped aggregations.

**5 — Units Sold by Region**
Grouped bar chart (interactive Plotly) comparing units sold per confectionary type across regions.

**6 — Profit Margin Analysis**
Calculates per-row profit margin (`Profit / Revenue`), aggregates by region and product, and visualises with:
- A bubble chart of average profit margin by country and product
- A grouped bar chart of highest vs. lowest margin per country

**7 — Seasonal Trends**
Identifies the peak sales month per product and plots monthly sales by country in a faceted bar chart with a country filter dropdown.

**8 — KPI Summary**
Prints top-level metrics: total revenue, total profit, average margin, and peak month overall.

**9 — Interactive Dash Dashboard**
A full browser-based dashboard with:
- Region and year dropdowns
- Product checklist filter
- Live KPI cards (revenue, profit, margin, units sold)
- Monthly sales trend line chart
- Revenue vs. profit margin bubble chart

---

## Running in JupyterLab

1. Open JupyterLab and navigate to this notebook.
2. Ensure `Confectionary [4564].xlsx` is in the same folder.
3. Run all cells: **Kernel → Restart Kernel and Run All Cells**.
4. The Dash app launches on `http://127.0.0.1:8050` — open this in your browser while the last cell is running.

> **Note:** The Dash server runs as a blocking process in the final cell. Keep the cell running while you use the dashboard. To stop it, interrupt the kernel (**Kernel → Interrupt**).

---

## Project Structure

```
.
├── Confectionary.ipynb         # Main notebook
├── Confectionary [4564].xlsx   # Source data (required)
└── README.md                   # This file
```
