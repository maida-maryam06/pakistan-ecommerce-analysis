# Pakistan E-Commerce Sales Data Analysis

A complete exploratory data analysis of Pakistan's largest e-commerce
dataset, covering 1M+ transactions from 2016–2018. Performed using
Pandas, Matplotlib, and Seaborn inside a Jupyter Notebook with 9
publication-quality visualizations and 5 actionable business insights.
Built as the Data Analysis task for the Enischyo Interns Python
Development internship program.

**Keywords:** python data analysis, pandas, matplotlib, seaborn,
jupyter notebook, pakistan ecommerce, exploratory data analysis,
data cleaning, data visualization, internship project.

## Dataset

**Name:** Pakistan's Largest E-Commerce Dataset  
**Source:** Kaggle — [zusmani/pakistans-largest-ecommerce-dataset](https://www.kaggle.com/datasets/zusmani/pakistans-largest-ecommerce-dataset)  
**Size:** 1,048,575 rows × 26 columns  
**Period:** July 2016 – August 2018  
**Fields:** order ID, status, date, category, price, quantity,
grand total, payment method, discount, customer ID, fiscal year

> Download the dataset from Kaggle and place the CSV in the same
> folder as the notebook before running.

## Quick start

```bash
git clone https://github.com/maida-maryam06/pakistan-ecommerce-analysis.git
cd pakistan-ecommerce-analysis
pip install -r requirements.txt
jupyter notebook pakistan_ecommerce_analysis.ipynb
```

## What's covered

### Data Loading & Exploration
- `shape`, `dtypes`, `head()`, `describe()` on the raw dataset
- Missing value counts and percentages per column
- Sample values per column to understand data quality

### Data Cleaning (every step documented with justification)
- Drop 5 fully-empty unnamed columns (100% NaN — no data)
- Drop rows missing all core transaction fields (~44% of raw data)
- Convert `created_at` and `Working Date` from strings to `datetime`
- Clean `MV` column — remove commas and spaces, convert to float
- Standardise payment methods — merge variants (e.g. `cod` +
  `cashatdoorstep` → `Cash on Delivery`)
- Remove duplicate `increment_id` rows
- Filter negative/zero `grand_total` values (refund adjustments)
- Separate completed vs non-completed orders for revenue analysis

### EDA Questions Answered

| Question | Visualization |
|----------|--------------|
| Which categories generate the most revenue? | Horizontal bar chart |
| Which category has the most orders? | Vertical bar chart |
| Average order value by payment method? | Bar chart with value labels |
| Which month has the highest sales? | Line chart + bar chart |
| What is the customer return rate? | Pie chart |
| Order value distribution and outliers? | Box plot + histogram |
| Order status breakdown? | Bar chart with percentages |
| Correlation between numeric features? | Heatmap |
| Payment method market share and revenue? | Pie + horizontal bar |

### 9 Visualizations
1. Top 10 categories by revenue (horizontal bar)
2. Orders by category (vertical bar)
3. Average order value by payment method (bar)
4. Monthly sales trend by year (line) + total per month (bar)
5. Customer return rate (pie)
6. Order value distribution by category (box plot) + histogram
7. Order status breakdown (bar with %)
8. Correlation heatmap
9. Payment method share (pie) + revenue (horizontal bar)

### 5 Business Insights (500-word summary)
1. Mobiles & Tablets dominate revenue but margins may be thin
2. Cash on Delivery dominates but carries operational risk
3. November is the peak sales month — seasonal surge opportunity
4. Low customer return rate signals a retention problem
5. Order cancellation rate is alarmingly high

## Project structure

```
pakistan-ecommerce-analysis/
├── pakistan_ecommerce_analysis.ipynb   # Main notebook
├── Pakistan_Largest_Ecommerce_Dataset.csv  # Dataset (download from Kaggle)
├── requirements.txt
└── README.md
```

PNG visualizations are saved automatically when you run the notebook.

## Running the notebook

```bash
# Install dependencies
pip install -r requirements.txt

# Option A — Jupyter in browser
jupyter notebook pakistan_ecommerce_analysis.ipynb

# Option B — VS Code
# Open the .ipynb file directly, select Python kernel, click Run All
```

Full execution takes 2–3 minutes due to the 1M+ row dataset.

## Key findings

- **Top revenue category:** Mobiles & Tablets
- **Most popular payment:** Cash on Delivery (46%+ of orders)
- **Peak sales month:** November (end-of-year campaign effect)
- **Completion rate:** ~40% of orders successfully complete
- **Cancellation rate:** ~34% — a major area for improvement
- **Customer retention:** Most customers place only 1 order

## Suggested GitHub topics

`python` `data-analysis` `pandas` `matplotlib` `seaborn`
`jupyter-notebook` `pakistan` `ecommerce` `data-visualization`
`data-cleaning` `eda` `internship-project`

## License

MIT
