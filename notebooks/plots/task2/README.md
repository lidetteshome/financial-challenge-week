## Task 2: Quantitative Stock Analysis (TA-Lib + yFinance)

This section focuses on applying financial data science to historical stock data for major tickers:  
**AAPL, AMZN, GOOG, META, MSFT, NVDA, TSLA**

---

### Tools & Libraries Used

- [`yfinance`](https://github.com/ranaroussi/yfinance) – to fetch price data
- `TA-Lib` – for technical indicators
- `matplotlib` – for plotting indicator behavior
- `pandas` – for data wrangling

---

### Data Preparation

- Fetched 3–6 months of historical data per stock
- Cleaned and formatted OHLCV data
- Calculated log/daily returns and rolling volatility

---

### Technical Indicators Calculated

| Indicator | Description |
|----------|-------------|
| `SMA (14)` | 14-day Simple Moving Average |
| `RSI (14)` | Relative Strength Index – tracks overbought/oversold zones |
| `MACD` | Moving Average Convergence Divergence, with signal & histogram |

All indicators were added as new columns in the price DataFrame per ticker.

---

### Visualizations Created

Each ticker has 6 charts saved under:

---

## Author

Lidet Teshome, 10 Academy AIM Cohort