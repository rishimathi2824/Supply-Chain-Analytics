# Supply Chain & Retail Performance Analysis

Exploratory data analysis of a global retail supply chain, turning ~180K order
records into business insights across market performance, inventory health,
operational efficiency, delivery reliability, profitability, and customer
satisfaction.

## Problem

Retail and supply-chain teams need a clear read on *where the business is winning
and where it's leaking* — which markets and categories drive sales, how fast and
accurately orders are fulfilled, how often deliveries run late, and which segments
are actually profitable. This project builds that read from raw order data.

## Dataset

Public **DataCo Smart Supply Chain** dataset, pulled directly from Kaggle at
runtime via `kagglehub` (no manual download or stored data files needed):
`shivkp/customer-behaviour`.

## Approach

- **Cleaning:** dropped fully-null and constant columns, removed duplicates,
  standardized column names, and reasoned carefully about which zero/null values
  were meaningful (e.g. same-day delivery) vs. noise before dropping anything.
- **Analysis areas:**
  - Market Performance — market share and category contribution to sales
  - Inventory Health
  - Operational Efficiency — order fulfillment time and processing accuracy
  - Shipping & Delivery — late-delivery risk rate and on-time delivery rate
  - Profitability — profit margin per order
  - Customer Satisfaction
- **Visualization:** matplotlib, seaborn, and squarify treemaps to make the
  patterns legible at a glance.

## Tools

Python · pandas · NumPy · matplotlib · seaborn · squarify · kagglehub

## How to run

```bash
pip install -r requirements.txt
jupyter notebook supply_chain_analysis.ipynb
```

The notebook downloads the dataset automatically on first run. (A free Kaggle
account / API token may be required by `kagglehub` — see Kaggle's docs.)

## Notes

This was originally built as a graduate analytics project and has been cleaned up
for sharing. The dataset is public and contains no proprietary or personal data.
