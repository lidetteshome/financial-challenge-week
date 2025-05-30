
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
ai-financial-sentiment/
├── data/                         # Input CSVs
├── outputs/                      # Metrics exports
│   └── yfinance_metrics/
├── plots/                        # Visual output
│   └── task1/
│   └── task2/
├── scripts/                      # Python analysis scripts
├── report/                       # Project reports
│   └── Week1_Task1_Task2_Report.docx
├── README.md
└── requirements.txt
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
