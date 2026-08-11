# RFM Customer Segmentation — Superstore Dataset

A Jupyter Notebook implementing RFM (Recency, Frequency, Monetary) analysis on
transactional retail data to segment customers by purchasing behavior.

## What this does
- Aggregates order-level transactions into per-customer Recency, Frequency,
  and Monetary metrics using pandas `.groupby().agg()`
- Scores each customer on a 1–5 quintile scale per dimension (`pd.qcut`),
  with Recency scored inversely so recent buyers rank highest
- Combines scores into a unified `RFM_Score` (e.g. `'555'`) and a summed
  `RFM_Total_Score` for ranking
- Includes markdown sections covering RFM theory, the quantile-scoring
  methodology (with academic references), and recommended visualizations
  (treemap, heatmap, bar chart, scatter) for presenting results

## Dataset
Sample Superstore sales data (2016–2019), ~793 unique customers.

## Requirements
`pandas`, `xlrd` (or `openpyxl`, depending on file format)
