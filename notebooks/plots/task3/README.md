
## Task 3: Correlation Between News Sentiment and Stock Movement

This task analyzes the relationship between financial news sentiment and daily stock returns.

---

### Sentiment Analysis
- Headlines were scored using `TextBlob` polarity.
- Sentiment scores were then averaged per day.

---

### Date Alignment & Returns
- Daily stock data from 7 tickers (AAPL, AMZN, GOOG, META, MSFT, NVDA, TSLA) were aligned by date.
- Daily returns were calculated as `% change` in closing prices.

---

### Correlation Analysis

#### Pearson Correlation:
- For each ticker, we calculated the Pearson correlation coefficient between:
  - **Average Daily Sentiment** vs. **Daily Return**
- Additional lag-based correlation was explored with +1 and +2 day shifts.

#### Rolling Correlation:
- A 30-day rolling window was applied to see how correlations evolve over time.

#### Sentiment Classes:
- Headlines were also classified as **Positive**, **Neutral**, or **Negative** based on polarity thresholds.

---

### Visualizations

Plots saved under `plots/task3/`:
- `correlation_barplot.png` – bar plot of correlation strength per ticker
- `*_sentiment_vs_return.png` – line plots of sentiment & returns
- `*_rolling_corr.png` – rolling 30-day correlations
- `lagged_correlation_barplot.png` – sentiment lags vs returns
- `sentiment_class_distribution.png` – stacked bar of sentiment classes

---

### Outputs

All data exports are stored in `outputs/task3/`:
- `*_sentiment_vs_return.csv`
- `sentiment_return_correlation_summary.csv`
- `lagged_sentiment_correlation.csv`
- `sentiment_class_distribution.csv`

---

## Author

Lidet Teshome, 10 Academy AIM Cohort