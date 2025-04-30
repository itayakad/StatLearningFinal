# StatLearningFinal

**StatLearningFinal** is a machine learning project that predicts whether a stock's price will go **up or down** based on recent **news sentiment and technical data**.

This project uses:
- 📰 News sentiment analysis via [FinBERT](https://huggingface.co/yiyanghkust/finbert-tone)
- 📈 Stock price data from [Alpha Vantage](https://www.alphavantage.co/)
- 🧠 A Random Forest classifier to learn stock behavior from sentiment + technical features

---

## 🚀 Features

- Pulls stock price data dynamically using Alpha Vantage's free API
- Gathers financial news using NewsAPI or fallback dummy articles
- Uses FinBERT (a BERT model fine-tuned for financial sentiment) to score news
- Creates labeled training data based on next-day price movement
- Trains and evaluates a binary classifier (`up` vs. `down`)
- Prints accuracy, precision, recall, and F1-score

---

## 📦 Requirements

```bash
pip install pandas numpy scikit-learn yfinance requests transformers torch
```

Also:
- Get a **free API key** from [Alpha Vantage](https://www.alphavantage.co/support/#api-key)
- Get a **free API key** from [NewsAPI.org](https://newsapi.org/)

---

## 📂 Usage

Edit and run the notebook:

```python
ticker = "AAPL"  # or "TSLA", "NVDA", etc.
```

Adjust the date range:

```python
from datetime import datetime, timedelta
end_date = datetime.today().date() - timedelta(days=1)
start_date = end_date - timedelta(days=90)
```

Then run the full pipeline:
- `get_stock_data()`
- `get_news_articles()`
- `analyze_sentiment()`
- `merge_and_label()`
- `train_and_evaluate()`

---

## 📊 Example Output

```
Accuracy: 0.57
Precision: 0.40
Recall: 1.00
```

---

## 🤝 Contributors

- Itay Akad
- Gilad Bejerano
- Nir Oren