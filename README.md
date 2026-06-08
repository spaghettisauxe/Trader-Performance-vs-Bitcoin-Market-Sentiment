# Trader Performance vs Bitcoin Market Sentiment

This project analyzes how trader performance changes across different Bitcoin market sentiment conditions.

I used historical trader data from Hyperliquid and matched each trade with the Bitcoin Fear & Greed Index value for that day. After combining both datasets, I compared trading performance across sentiments like Fear, Greed, Neutral, and Extreme Greed.

## What This Project Does

The main goal was to check whether market sentiment has any visible relationship with trader behavior and performance.

I looked at questions like:

* Do traders make more or less money during Fear or Greed?
* Do traders trade more during certain sentiment conditions?
* Does average trade size change with market sentiment?
* Which coins perform better under specific sentiments?
* Do BUY/SELL trades behave differently during Fear or Greed?

## Datasets

This project uses two datasets:

1. **Historical Trader Data**

   * Contains trade-level data from Hyperliquid.
   * Important columns include account, coin, side, size, timestamp, fee, and closed PnL.

2. **Bitcoin Fear & Greed Index**

   * Contains daily sentiment data.
   * Important columns include date, sentiment value, and classification.

## Process

The project follows a simple workflow:

1. Load both datasets
2. Clean and convert date columns
3. Create a common date column
4. Merge trader data with sentiment data
5. Remove rows where sentiment was not available
6. Analyze performance by sentiment
7. Create plots for the main metrics
8. Write observations from the results

## Analysis Performed

The notebook includes analysis for:

* Average Closed PnL by sentiment
* Total Closed PnL by sentiment
* Trade count by sentiment
* Win rate by sentiment
* Average trade size by sentiment
* Coin-wise performance by sentiment
* Side-wise performance by sentiment
* Top coin and sentiment combinations by average PnL

## Tools Used

* Python
* pandas
* matplotlib
* Jupyter Notebook

## How to Run

Clone the repository:

```bash
git clone <your-repo-url>
cd <your-repo-name>
```

Install the required libraries:

```bash
pip install pandas matplotlib jupyter
```

Open the notebook:

```bash
jupyter notebook
```

Then run the notebook cells from top to bottom.

## Project Structure

```text
.
├── notebook.ipynb
├── README.md
├── data/
│   ├── historical_trader_data.csv
│   └── fear_greed_index.csv
└── plots/
```

## Note

Some trades did not have matching sentiment data because the trader dataset and sentiment dataset did not fully overlap by date. For the final analysis, I used only the trades where sentiment data was available.

## Summary

This project explores the relationship between market sentiment and trader performance. The analysis focuses on simple trading metrics like PnL, win rate, trade count, trade size, and coin-wise performance to understand how trading behavior changes under different market moods.
