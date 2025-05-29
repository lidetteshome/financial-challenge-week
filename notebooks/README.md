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

. <br>
├── LICENSE <br>
├── README.md <br>
├── data <br>
│   ├── AAPL_historical_data.csv <br>
│   ├── AMZN_historical_data.csv <br>
│   ├── GOOG_historical_data.csv <br>
│   ├── META_historical_data.csv <br>
│   ├── MSFT_historical_data.csv <br>
│   ├── NVDA_historical_data.csv <br>
│   ├── TSLA_historical_data.csv <br>
│   └── raw_analyst_ratings.csv <br>
├── notebooks <br>
│   ├── README.md <br>
│   ├── __init__.py <br>
│   └── financial_eda.ipynb <br>
├── requirements.txt <br>
├── scripts <br>
│   ├── README.py <br>
│   ├── __init__.py <br>
│   ├── financial_eda.py <br>
│   ├── quantitative_analysis.py <br>
│   └── sentiment_analysis.py <br>
├── src <br>
│   └── __init__.py <br>
└── tests <br>
    └── __init__.py <br>

---

## 🧪 Run Unit Tests

```bash
pytest tests/

✍️ Author

Lidet Teshome, 10 Academy AIM Cohort