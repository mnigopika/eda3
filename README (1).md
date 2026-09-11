# 📈 Shopify (SHOP) Stock — Exploratory Data Analysis

Exploratory data analysis of Shopify (SHOP) historical stock price data, covering data cleaning, feature engineering, and visualization of price and volume trends.

## 🔍 Overview

This notebook (`Task3EDA.ipynb`) performs an end-to-end EDA workflow on daily Shopify stock data:

- Loads and inspects the raw dataset
- Cleans missing values and duplicate rows
- Parses and sorts data by date
- Engineers derived financial metrics
- Computes summary statistics
- Visualizes trading volume, price range, and return distribution

## 🗂️ Dataset

- **File:** `SHOP_2015-05-21.csv`
- **Expected columns:** `date`, `open`, `high`, `low`, `close`, `volume`
- The notebook expects the CSV at `/content/SHOP_2015-05-21.csv` (default Google Colab path). Update this path if running locally.

## ⚙️ Workflow

1. **Load & Inspect** — read the CSV, check shape, dtypes, and null counts
2. **Clean** — drop duplicate rows, parse `date` to datetime, drop rows with invalid/missing values, sort and set `date` as the index
3. **Feature Engineering**
   - `Daily_Price_Change` = `close` − `open`
   - `Daily_Return_%` = `(close − open) / open × 100`
   - `Price_Range` = `high` − `low`
4. **Statistics** — descriptive stats, variance and standard deviation of daily returns
5. **Visualization**
   - Trading volume trend over time
   - Distribution of daily returns (histogram)
   - Price range trend over time

## 📦 Requirements

```bash
pip install pandas matplotlib
```

## ▶️ Usage

1. Place `SHOP_2015-05-21.csv` in the working directory (or update the file path in the notebook).
2. Open and run `Task3EDA.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
3. Run all cells sequentially to reproduce the cleaning steps, statistics, and charts.

## 📊 Output

- Console summaries: dataset info, null counts, descriptive statistics, return variance/standard deviation
- Charts: volume trend, daily return distribution, price range trend

<!--
## 🖼️ Sample Charts
Add screenshots of your generated plots here, e.g.:
![Volume Trend](images/volume_trend.png)
![Return Distribution](images/return_distribution.png)
![Price Range Trend](images/price_range_trend.png)
-->

## 📄 License

Add a license of your choice (e.g., MIT) if distributing this project publicly.
