# E-Commerce Analytics Dashboard

An end-to-end Power BI portfolio project — from raw, messy transactional data to a fully modeled, 7-page interactive dashboard with real, verified business findings.

## Overview

This project analyzes e-commerce performance across customers, campaigns, transactions, and products for a synthetic dataset spanning **Jan 2021 – Dec 2023** (100,000 customers, 103,127 transactions, 100,000 events, 2,000 products, 50 campaigns).

The focus wasn't just building charts — it was building a **correct, verified data model** first, then surfacing findings that actually hold up when you check them against the raw data.

## Dashboard Pages

| Page | What it covers |
|---|---|
| **Cover** | Branded landing page |
| **Executive Overview** | Revenue, orders, customers, and conversion funnel at a glance |
| **Customer Insights** | Demographics, loyalty tier value analysis, retention |
| **Campaigns & Events** | Channel performance, conversion rate heatmap by traffic source × device, funnel |
| **Transactions** | Revenue waterfall, order status breakdown, quarterly trends, transaction-level detail |
| **Product** | Category/price-tier performance, premium vs. non-premium comparison, interactive decomposition tree |
| **Strategic Insights** | 6 key findings with a bookmark-driven Findings ↔ Recommendations toggle |

## Key Findings

- **Premium pricing works** — premium products are 50% of the catalog but generate 77% of revenue, on nearly identical unit volume to non-premium items.
- **Q4 carries the business** — Q4 alone accounts for 28.8% of annual revenue, well above the 25% an evenly-distributed quarter would produce.
- **Organic traffic underperforms** — drives 41% of all sessions but converts at just 2.1%, roughly a quarter of the rate of Paid Search and Email.
- **Reactivation beats Acquisition** — campaigns targeting lapsed customers generated $1.96M vs. $1.31M for new-customer acquisition campaigns.
- **Revenue is flat, not growing** — a slow year-over-year decline (2021 → 2023) sits underneath what looks like a healthy 3-year chart at first glance.
- **10% of orders never complete** — 10,449 transactions carry no product and $0 revenue, a data-capture issue worth investigating rather than silently filtering out.

## Data Modeling & Engineering

- Cleaned corrupted source data: mislabeled columns from a bad global find-and-replace, incorrect data types across three tables, and a broken auto-date relationship that was silently matching 11 of 103,000+ rows.
- Built a proper star schema: 6 fact/dimension tables, a custom Date table (replacing Power BI's auto-date), and correctly scoped active/inactive relationships to avoid ambiguous filter paths.
- 40+ DAX measures organized in a dedicated `_Measures` table across Revenue, Customers, Marketing, Product, and Time Intelligence folders.
- 10+ calculated columns, including custom sort-key columns to fix chronological/tier ordering that would otherwise sort alphabetically or by value instead of logically.

## Interactive Features

- Custom sidebar navigation with active-page highlighting, built once and replicated across all 7 pages.
- A **Decomposition Tree** on the Product page with a native measure switcher (Revenue ↔ Units Sold).
- A **bookmark-driven toggle** on the Strategic Insights page switching every card between "Key Finding" and "Recommendation" text.
- Conditional formatting throughout (heatmap matrix, trend indicators, order status coloring).

## Tech Stack

- Power BI Desktop
- DAX (measures, calculated columns, time intelligence)
- Power Query (M) for data cleaning and transformation
- Star schema data modeling



## Author

**Kartikey Singh**
