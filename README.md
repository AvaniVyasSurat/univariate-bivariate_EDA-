# Univariate, Bivariate & Multivariate Analysis — Walmart Sales

A visualization-focused EDA project on a 1,000-row Walmart-style sales dataset using **Python**, **Pandas**, and **Matplotlib**, practicing univariate, bivariate, and multivariate analysis through bar charts, pie charts, histograms, and scatter plots.

## 📊 About the Dataset

File: `9-univariate-bivariate-multivariate.csv` — 1,000 rows × 17 columns.

| Column | Renamed To | Description |
|---|---|---|
| Invoice ID | invoiceID | Unique invoice number |
| Branch | — | Branch (A, B, C) |
| City | — | City of the branch |
| Customer type | customertype | Member or Normal |
| Gender | — | Gender of the customer |
| Product line | product_line | Product category |
| Unit price | unit_price | Price per unit |
| Quantity | — | Number of units purchased |
| Tax 5% | tax_5 | 5% tax on the transaction |
| Total | — | Total price including tax |
| Date | — | Date of purchase |
| Time | — | Time of purchase |
| Payment | — | Payment method |
| cogs | — | Cost of goods sold |
| gross margin percentage | — | Gross margin % |
| gross income | gross_income | Gross income earned |
| Rating | — | Customer's rating (1–10) |

No missing values — all 17 columns have 1,000 non-null entries.

## 🎯 Purpose

To practice and demonstrate the three core types of exploratory analysis on a single dataset:
- **Univariate** — examining one variable at a time (e.g., distribution of COGS, Total sales, customer ratings).
- **Bivariate** — examining the relationship between two variables (e.g., COGS vs. Total, gross income vs. Rating).
- **Multivariate/grouped** — examining a variable broken down by a categorical dimension (e.g., gross income by branch, sales by payment method and product line).

## 🛠️ Approach

1. **Load and inspect** the dataset — shape, structure, columns.
2. **Rename columns** to snake_case for easier, more consistent access.
3. **Univariate analysis** — histograms of `cogs` and `Total`; value counts and pie/bar charts for `customertype`, `Rating`, `City`, `product_line`.
4. **Bivariate analysis** — scatter plots of `cogs` vs. `Total` and `gross_income` vs. `Rating`.
5. **Grouped/multivariate analysis** — bar and pie charts of `Total`/`gross_income`/`Quantity` broken down by `Branch`, `Gender`, `product_line`, `City`, `customertype`, and `Payment`.
6. **Aggregation** — `groupby()` on `product_line` and `unit_price` to rank product lines and analyze sales by price.
7. **Filtering** — count invoices for a specific combination of `product_line` and `Gender`.

## ❓ Questions Answered

- What does the dataset look like, and what is its shape and structure?
- How is total sales distributed by branch and by payment method?
- What's the relationship between COGS and Total sales?
- How does gross income vary by gender and by product line?
- How does customer rating vary by city?
- How is total sales distributed by customer type?
- What's the distribution (histogram) of COGS and of Total sales?
- What's the breakdown of customer types (pie chart)?
- How does total sales change with unit price?
- Which product lines have the highest summed unit price?
- How many Fashion Accessories purchases were made by female customers, and in total?
- How is total quantity sold distributed across product lines?
- What's the frequency distribution of customer ratings?
- What's the relationship between gross income and rating (scatter plot)?
- How is gross income distributed by branch?
- How is sales volume distributed by city (pie chart)?
- What's the distribution of product lines by invoice count (pie chart)?

## 🗄️ Tech Stack

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

## 📁 Repository Structure

```
├── 9_univariateproject.ipynb   # Notebook with code, outputs, and visualizations
├── Project_Report.docx         # Full project report
└── README.md
```

## 🚀 How to Run

1. Install the requirements:
   ```
   pip install pandas numpy matplotlib jupyter
   ```
2. Place `9-univariate-bivariate-multivariate.csv` in the working directory (update the file path in the notebook if needed — the original path points to a Google Drive mount).
3. Open and run the notebook:
   ```
   jupyter notebook 9_univariateproject.ipynb
   ```

**Note:** A couple of cells in the original notebook contain minor bugs — assigning a string to `pl.xlabel`/`pl.ylabel` instead of calling them as functions (e.g., `pl.xlabel("cogs")` is correct, `pl.xlabel = "cogs"` is not), and a bar chart that mixes a Series (`x`) with a single summed value (`y`). These are flagged inline in the notebook and should be corrected before relying on those specific plots.

## 📌 Key Findings

- The dataset has **1,000 transactions** across **17 columns**, with **no missing values**.
- **Fashion accessories** has the highest summed unit price (**10,173.35**), narrowly ahead of **Food and beverages** (9,745.54).
- Of all Fashion Accessories invoices, **96 out of 178** (about 54%) were purchased by **female customers**.
- Sales (`Total`) and `unit_price` both show wide variation, visualized via histograms and grouped sums.
- Gross income, ratings, and sales all vary meaningfully across **branch**, **city**, **gender**, and **product line** — explored through a dedicated bar or pie chart for each.

---
*A univariate, bivariate, and multivariate exploratory analysis project on Walmart-style sales data.*
