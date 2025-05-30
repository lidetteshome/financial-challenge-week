
# Financial News & Stock Indicator Analysis

Week 1 – 10 Academy AIM Program  
Author: Lidet Teshome
Email: lidet.teshome.aastu@gmail.com

---

## Project Overview

This project investigates the relationship between financial news headlines and stock market movements. We explore both the **qualitative patterns in news** and **quantitative indicators in stock prices** to identify potential trading signals and sentiment-driven trends.

---

## Task 1: News Dataset EDA & Sentiment Analysis

We performed exploratory data analysis (EDA) on a dataset of financial headlines and publishers.

### Descriptive Statistics

- Calculated headline lengths and visualized distribution
- Observed that most headlines are concise, ~80–120 characters

### Publisher Behavior

- Identified top 15 publishers by frequency
- Sampled headlines from major sources
- Extracted email-style domains (e.g., `@reuters.com`) when present

### Time Series Analysis

- Daily article counts showed peaks during key events (e.g., COVID crash)
- Time-of-day distribution revealed most articles published between 8–10am UTC

### Text Analysis (Topic Modeling)

- Extracted top unigrams and bigrams using `CountVectorizer`
- Common terms: `"price target"`, `"FDA approval"`, `"quarter earnings"`

### Visualizations

Saved under: `plots/task1/`

- Headline length histogram
- Top publishers bar chart
- Daily publishing volume (global + COVID window)
- Hour-of-day publishing heatmap
- Top 20 keyword phrases

---

## Task 2: Quantitative Stock Analysis

Analyzed stock price data for 7 major tickers:

**AAPL, AMZN, GOOG, META, MSFT, NVDA, TSLA**

### Data Source

- Pulled 6 months of historical OHLCV data via `yfinance`

### Technical Indicators (TA-Lib)

| Indicator | Purpose |
|----------|---------|
| SMA (14) | Trend tracking (short-term) |
| RSI (14) | Overbought/oversold identification |
| MACD     | Momentum and crossover analysis |

### Financial Metrics

- Current price
- Daily return mean & std. dev
- 14-day rolling volatility

Saved to: `outputs/yfinance_metrics/`

### Enhanced Visualizations

Saved under: `plots/task2/impact_analysis/`

- **Close Price + SMA zones** (bullish/bearish)
- **RSI signals** (highlighting >70 and <30 zones)
- **MACD crossovers** (with histogram, signal line)

Example:  
```
plots/task2/impact_analysis/AAPL_price_sma_zone.png
plots/task2/impact_analysis/AMZN_rsi_signals.png
```

---

## Folder Structure

```
.
├── LICENSE
├── README.md
├── data
│   ├── AAPL_historical_data.csv
│   ├── AMZN_historical_data.csv
│   ├── GOOG_historical_data.csv
│   ├── META_historical_data.csv
│   ├── MSFT_historical_data.csv
│   ├── NVDA_historical_data.csv
│   ├── TSLA_historical_data.csv
│   └── raw_analyst_ratings.csv
├── notebooks
│   ├── __init__.py
│   ├── financial_eda.ipynb
│   ├── outputs
│   │   └── yfinance_metrics
│   │       ├── AAPL_metrics.csv
│   │       ├── AMZN_metrics.csv
│   │       ├── GOOG_metrics.csv
│   │       ├── META_metrics.csv
│   │       ├── MSFT_metrics.csv
│   │       ├── NVDA_metrics.csv
│   │       ├── TSLA_metrics.csv
│   │       └── summary_metrics.csv
│   ├── plots
│   │   ├── task1
│   │   │   ├── README.md
│   │   │   ├── covid_crash_volume.png
│   │   │   ├── daily_news_volume.png
│   │   │   ├── headline_length_distribution.png
│   │   │   ├── hourly_distribution.png
│   │   │   ├── top_publishers.png
│   │   │   └── topic_keywords.png
│   │   └── task2
│   │       ├── AAPL_indicators.png
│   │       ├── AMZN_indicators.png
│   │       ├── GOOG_indicators.png
│   │       ├── META_indicators.png
│   │       ├── MSFT_indicators.png
│   │       ├── NVDA_indicators.png
│   │       ├── README.md
│   │       ├── TSLA_indicators.png
│   │       ├── impact_analysis
│   │       │   ├── AAPL_macd_crossovers.png
│   │       │   ├── AAPL_price_sma_zone.png
│   │       │   ├── AAPL_rsi_signals.png
│   │       │   ├── AMZN_macd_crossovers.png
│   │       │   ├── AMZN_price_sma_zone.png
│   │       │   ├── AMZN_rsi_signals.png
│   │       │   ├── GOOG_macd_crossovers.png
│   │       │   ├── GOOG_price_sma_zone.png
│   │       │   ├── GOOG_rsi_signals.png
│   │       │   ├── META_macd_crossovers.png
│   │       │   ├── META_price_sma_zone.png
│   │       │   ├── META_rsi_signals.png
│   │       │   ├── MSFT_macd_crossovers.png
│   │       │   ├── MSFT_price_sma_zone.png
│   │       │   ├── MSFT_rsi_signals.png
│   │       │   ├── NVDA_macd_crossovers.png
│   │       │   ├── NVDA_price_sma_zone.png
│   │       │   ├── NVDA_rsi_signals.png
│   │       │   ├── TSLA_macd_crossovers.png
│   │       │   ├── TSLA_price_sma_zone.png
│   │       │   └── TSLA_rsi_signals.png
│   │       └── indicators
│   │           ├── AAPL_indicators.png
│   │           ├── AMZN_indicators.png
│   │           ├── GOOG_indicators.png
│   │           ├── META_indicators.png
│   │           ├── MSFT_indicators.png
│   │           ├── NVDA_indicators.png
│   │           └── TSLA_indicators.png
│   └── technical_analysis.ipynb
├── requirements.txt
├── scripts
│   ├── README.py
│   ├── __init__.py
│   ├── financial_eda.py
│   ├── quantitative_analysis.py
│   └── sentiment_analysis.py
├── src
│   └── __init__.py
└── tests
    └── __init__.py

```

---

## Requirements

Install everything with:

```bash
pip install -r requirements.txt
```

Key packages:
- `pandas`, `matplotlib`, `seaborn`
- `yfinance`, `TA-Lib`
- `scikit-learn`, `wordcloud`
- `transformers` (for future sentiment models)

---

## Next Steps

- Streamlit dashboard for real-time news + price indicator syncing
- Add Bollinger Bands, EMA, or SAR indicators
- Integrate sentiment classification (BERT/FinBERT)

---

## Author

Lidet Teshome – 10 Academy AIM Cohort  
