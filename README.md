# IBEX Market Data Scraper - Databricks Project

This project extracts Day-Ahead electricity market data from the [IBEX website](https://ibex.bg/markets/dam/day-ahead-prices-and-volumes-v2-0-2/) using Selenium and BeautifulSoup, structures it with PySpark, and stores the cleaned tables as Delta tables in Databricks.

## What the Notebook Does

- Sets up headless Chrome using `selenium` on Databricks.
- Scrapes 3 tables from the target URL:
  1. Prices and Volumes
  2. Block Products (Base / Peak / Off-Peak)
  3. Hourly Products
- Cleans and transforms the scraped data.
- Writes each cleaned table to separate Delta tables:
  - `prices_volumes_table`
  - `block_products_table`
  - `hourly_products_table`

## Libraries Used

- `selenium`, `webdriver-manager`, `beautifulsoup4`
- `pyspark.sql` for Spark DataFrame operations

## How to Run

1. Install required libraries and Chrome (already included in notebook).
2. Run the notebook in a Databricks environment.
3. Use the `display()` commands to view the tables, or query them via SQL.

## Output

You will see three Delta tables in your Databricks workspace:
- 📊 `prices_volumes_table`
- 🧱 `block_products_table`
- ⏱️ `hourly_products_table`

---

Author: Gowthami Urs  
Date: June 11, 2025
