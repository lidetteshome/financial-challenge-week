# 📈 Financial News Sentiment & Stock Movement Analysis

Welcome to the Week-1 Challenge of 10 Academy AIM Program: Using NLP & Market Data to uncover alpha.

---

## 🚀 Objective

Explore correlations between financial news sentiment and daily stock returns across major tickers (AAPL, AMZN, GOOG, etc.) using:

- 📊 Technical indicators  
- 🤖 Transformer-based sentiment analysis  
- 📉 Return calculations and statistical correlation

---

## 🧠 Tasks Completed

### Task 1: EDA on News Dataset

#### 🔍 Descriptive Statistics
- Headline length calculated for all articles  
- Histogram plotted to visualize length distribution  

#### 📰 Publisher Analysis
- Top 15 publishers by article count identified and plotted  
- Sample headlines from top publishers reviewed  
- Checked for email-style publisher entries, extracted domains  

#### ⏰ Time Series Analysis
- Daily publishing frequency plotted to identify spikes  
- Zoomed in on COVID-19 crash period (Feb–Apr 2020)  
- Hour-of-day analysis showed most articles are published between 8am–10am UTC  

#### 🧠 Text Analysis (Topic Modeling)
- `CountVectorizer` used to extract common unigrams and bigrams  
- Frequent terms like `"price target"`, `"fda approval"` identified  
- Bar plot of top 20 keyword phrases visualized  

---

## Task 2: Technical Stock Analysis

See separate section.

---

## 📁 Folder Structure

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
│   ├── README.md
│   ├── __init__.py
│   └── financial_eda.ipynb
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

---

## 🧪 Run Unit Tests

```bash
pytest tests/

✍️ Author

Lidet Teshome, 10 Academy AIM Cohort