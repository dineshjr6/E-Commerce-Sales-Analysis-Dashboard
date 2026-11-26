# E-Commerce Sales Analysis Dashboard

A Python data analysis project that cleans an Amazon India sales report (~129K orders) and turns it into sales trends, category and product insights, geographic breakdowns, fulfilment analysis, and a single combined dashboard.

## Dataset

**Amazon Sale Report** (`Amazon Sale Report.csv`) — 128,975 order rows with columns including:

`Order ID`, `Date`, `Status`, `Fulfilment`, `Sales Channel`, `ship-service-level`, `Style`, `SKU`, `Category`, `Size`, `ASIN`, `Courier Status`, `Qty`, `currency`, `Amount`, `ship-city`, `ship-state`, `ship-postal-code`, `ship-country`, `promotion-ids`, `B2B`, `fulfilled-by`

The raw CSV is not included in this repo. Download it separately and update the path in the first cell of `ecom.ipynb`.

## What's Inside

| File | Description |
|------|-------------|
| `ecom.ipynb` | Main notebook: data cleaning, analysis tasks, and the final dashboard |
| `trendanalize.ipynb` | Scratch notebook for trend analysis (currently empty) |

## Analysis Workflow

1. **Data cleaning**
   - Parse `Date` into datetime
   - Standardize `ship-state` (trim whitespace, uppercase)
   - Fill missing `Amount`, `Courier Status` (mode), and `currency` (`INR`)
   - Export the result to `cleaned_data.csv`
2. **Sales trend analysis**: monthly revenue, best and worst months, month-over-month growth, line chart
3. **Category and product performance**: top and bottom categories, quantity vs. revenue, most popular size per category, revenue bar chart
4. **Geographical analysis**: top 10 states by orders and by revenue, horizontal bar chart
5. **Order status and fulfilment**: status distribution (pie chart), fulfilment type vs. order status
6. **Dashboard**: a 3×2 grid combining monthly trend, revenue by category, top states, order status, fulfilment vs. status, and quantity by category

## Tech Stack

- Python 3
- pandas
- matplotlib
- Jupyter Notebook

## Getting Started

```bash
# 1. Clone the repo
git clone https://github.com/dineshjr6/E-Commerce-Sales-Analysis-Dashboard.git
cd E-Commerce-Sales-Analysis-Dashboard

# 2. Install dependencies
pip install pandas matplotlib jupyter

# 3. Add the dataset and update the file path in the first cell of ecom.ipynb

# 4. Launch the notebook
jupyter notebook ecom.ipynb
```

Run the cells top to bottom. The cleaning section must run first, since later analysis depends on the cleaned `df`.

## Author

**Dineshwaran J R** — AI developer, Chennai, India
GitHub: [@dineshjr6](https://github.com/dineshjr6)
