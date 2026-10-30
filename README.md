# Interactive sales report

Monthly sales dashboard for Hartwell Flow Systems, a fictional pump and valve manufacturer.

Live site: https://interactive-sales-report.netlify.app

## Data

The dashboard reads the CSV files in `data/` when the page opens. The data runs from July 2023 to September 2026.

| File | One row per | Main columns |
|---|---|---|
| `quotes.csv` | quote | customer, sales rep, product category, value, inquiry and sent dates, status (won, lost, open), won or lost reason, and for won quotes the order, invoice date, gross margin, return and survey answer |
| `customers.csv` | customer | region, sales rep |
| `sales_reps.csv` | sales rep | region |
| `targets_and_forecasts.csv` | month, sales rep and product category | revenue target, revenue forecast |
| `quarterly_measures.csv` | quarter | cost of sales as a share of revenue, customer retention, sales team turnover, win rate |
| `sales_funnel.csv` | stage of the sales process | opportunities in the latest quarter |

To change what the dashboard shows, edit or replace these files and keep the column names.

## Updating the site

Commit and push to `main`. Netlify publishes every push to `main`.

## Preview locally

The page loads its data with `fetch`, so open it through a local web server rather than as a file:

```bash
python3 -m http.server 8000
```

Then go to http://localhost:8000.
