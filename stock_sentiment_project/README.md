# 📈 Stock Market Sentiment Analysis Pipeline

An end-to-end AI-powered data analytics project that fetches live stock prices and real financial news headlines, applies **FinBERT NLP model** for sentiment classification, joins data using **SQL**, and visualizes insights in an interactive **Power BI dashboard**.

---

## 🎯 Project Objective

> **"Does positive or negative news about a stock correlate with its price movement?"**

This project answers that question by combining real-time financial data with AI-powered natural language processing — the same approach used by quantitative finance teams.

---

## 🏗️ Project Architecture

```
yfinance (Stock Prices)
        │
        ▼
NewsAPI (News Headlines)
        │
        ▼
FinBERT NLP Model (AI Sentiment Analysis)
        │
        ▼
SQLite (Data Engineering & SQL Joins)
        │
        ▼
Power BI (Interactive Dashboard)
```

---

## 🛠️ Tech Stack

| Layer | Tool | Purpose |
|---|---|---|
| Stock Data | `yfinance` | Fetches real-time OHLCV data from Yahoo Finance |
| News Data | `NewsAPI` | Fetches live financial news headlines |
| AI Model | `FinBERT` | Domain-specific NLP model for financial sentiment |
| Data Storage | `SQLite` | Stores and joins datasets using SQL |
| Data Processing | `Pandas` | Data cleaning and transformation |
| Visualization | `Power BI` | Interactive dashboard |
| Environment | `Google Colab` | Cloud-based Python notebook |

---

## 📊 Dashboard Features

- **Stock Price Cards** — Latest price for AAPL, GOOGL, MSFT, AMZN, TSLA
- **Sentiment Score by Stock** — Which stock has the most positive/negative news
- **AI Confidence Score** — How confident FinBERT was in its classifications
- **Sentiment Breakdown** — Overall split of Positive / Neutral / Negative
- **Headlines Table** — Every headline with its AI sentiment label and confidence score

---

## 🤖 AI Integration — FinBERT

This project uses **FinBERT** (`ProsusAI/finbert`), a BERT-based transformer model fine-tuned specifically on financial text including Bloomberg articles, Reuters news, and earnings reports.

Unlike general-purpose sentiment models, FinBERT understands financial context:
- *"Apple faces antitrust probe"* → **Negative** (0.95 confidence)
- *"Apple Looking to Add MacBook Neo"* → **Positive** (0.90 confidence)
- *"Paul Tudor Jones Warns Market Boom"* → **Neutral** (0.70 confidence)

---

## 📁 Project Structure

```
stock-sentiment-analysis/
│
├── stock_sentiment_pipeline.ipynb   # Main Colab notebook
├── stock_sentiment_final.csv        # Detailed sentiment + price data
├── stock_summary.csv                # Summary table per stock
├── Stock_Sentiment_Dashboard.pbix   # Power BI dashboard file
└── README.md                        # Project documentation
```

---

## ⚙️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/stock-sentiment-analysis.git
```

### 2. Open in Google Colab
- Upload `stock_sentiment_pipeline.ipynb` to [colab.research.google.com](https://colab.research.google.com)

### 3. Add API Keys in Colab Secrets
- `NEWS_API_KEY` → Get free key from [newsapi.org](https://newsapi.org)
- FinBERT runs locally — no API key needed

### 4. Run all cells in order
```
Cell 1 → Install libraries
Cell 2 → Load API keys
Cell 3 → Fetch stock prices (yfinance)
Cell 4 → Fetch news headlines (NewsAPI)
Cell 5 → Run FinBERT sentiment analysis
Cell 6 → SQL join and data engineering
Cell 7 → Export CSVs
```

### 5. Load CSVs into Power BI
- Open `Stock_Sentiment_Dashboard.pbix` in Power BI Desktop
- Or load the CSV files manually into a new Power BI report

---

## 📈 Sample Output

| Ticker | Sentiment | Confidence | Close Price |
|--------|-----------|------------|-------------|
| AAPL | positive | 0.90 | $293.32 |
| GOOGL | neutral | 0.91 | $400.80 |
| MSFT | positive | 0.89 | $415.12 |
| AMZN | positive | 0.95 | $283.00 |
| TSLA | negative | 0.85 | $360.84 |

### Sentiment Summary

| Ticker | Positive | Neutral | Negative | Sentiment Score |
|--------|----------|---------|----------|-----------------|
| AAPL | 3 | 5 | 2 | 0.10 |
| GOOGL | 3 | 6 | 1 | 0.20 |
| MSFT | 3 | 5 | 2 | 0.10 |
| AMZN | 3 | 5 | 1 | 0.22 |
| TSLA | 3 | 6 | 1 | 0.20 |

---

## 🔮 Future Improvements

- [ ] Expand to 20+ stocks
- [ ] Add historical sentiment trend over 90 days
- [ ] Implement price movement prediction using sentiment score
- [ ] Schedule pipeline to run daily automatically
- [ ] Add email alert when sentiment drops sharply

---

## 👤 Author

**Your Name**
- LinkedIn: [linkedin.com/in/yourprofile](https://www.linkedin.com/in/mohit-sengar-16096a2bb/)
- GitHub: [github.com/yourusername](https://github.com/mohit27-maker)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
