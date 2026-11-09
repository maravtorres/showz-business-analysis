# Showz — Business Analysis

Business analysis for Showz, a ticket sales platform: user behavior, sales and marketing spend, to help optimize advertising investment.

TripleTen Data Analyst program project — Mara Torres Blanco.

## What this project does

Using user sessions, orders and marketing costs (January 2017 – December 2018), this project:

1. **Cleans and prepares the data** (column names, datetime types, auxiliary week/month/session-duration columns).
2. **Measures user behavior**: DAU/WAU/MAU, session length, device split, cohort retention and time to first purchase.
3. **Measures sales**: orders per month, average order value (AOV) and lifetime value (LTV) by cohort.
4. **Measures marketing efficiency**: total spend, customer acquisition cost (CAC) and return on marketing investment (ROMI) per source.
5. **Closes with recommendations** for the marketing team, including which sources deserve more budget.

## Tools

- Python
- Pandas, NumPy
- Matplotlib, Seaborn

## Key findings

### User behavior

- Traffic has **strong seasonality**, with peaks in **November and December**, the high season for events.
- Most sessions are **short (under 5 minutes)**: users arrive with a clear, specific purchase intent.
- **Desktop sessions are longer** than mobile, suggesting users prefer to complete purchases from a computer.
- **Retention beyond month 1 is low**, which is structural to the business: users buy tickets for one-off events and do not necessarily come back often.

### Sales and conversion

- A **large share of users buy on the same day** as their first visit, showing acquisition channels bring high-intent audiences.
- **LTV grows cumulatively**, but the most important revenue comes in the **first two months** after the first visit.
- **More recent cohorts show higher LTV**, which may reflect improvements in the event offer or audience segmentation.
- **AOV is stable** over time, with occasional peaks matching higher-value events.

### Marketing

- The budget is **concentrated in a few sources**, a risk if one of them fails or raises its cost.
- Some sources have **negative ROMI**: they consume budget without generating enough revenue.
- Sources with **low CAC and high ROMI** are the most efficient and should receive more investment.
- Marketing spend is **not always aligned with demand peaks** (November–December), an opportunity for improvement.

### Recommendations

- Invest more in sources that combine **high ROMI, low CAC and high month-0 LTV**; pause or renegotiate sources that fail all three criteria.
- Align marketing spend with the November–December demand peaks.

## Data

- `visits_log_us.csv` — user sessions (January 2017 – December 2018).
- `orders_log_us.csv` — orders placed.
- `costs_us.csv` — marketing spend by source.

**The datasets are not included in this repository** — they were provided on the TripleTen learning platform. The notebook will not run without them; the code and outputs are preserved as delivered.

## Files

- `showz_business_analysis.ipynb` — the analysis notebook (78 cells).
- `README.md` — this file.

## How to run

Open `showz_business_analysis.ipynb` in Jupyter Notebook or JupyterLab and run the cells top to bottom. It expects `visits_log_us.csv`, `orders_log_us.csv` and `costs_us.csv` in the same folder (not included — see Data above).
