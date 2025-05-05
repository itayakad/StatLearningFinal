# StatLearningFinal

**StatLearningFinal** is a machine learning pipeline designed to predict **next-day stock returns** using a combination of **news sentiment** and **technical indicators**, and simulate trades based on the model’s predictions.

This project includes:
- 📥 News collection via [Alpaca Markets](https://alpaca.markets/)
- 💬 Sentiment analysis using [VADER](https://github.com/cjhutto/vaderSentiment)
- 📈 Technical feature generation using the `ta` library
- 🤖 Predictive modeling with XGBoost
- 💰 Trade simulation based on predicted position sizing

---

## 🚀 Features

- Dynamically collects stock-specific news headlines using Alpaca's API
- Assigns sentiment scores to headlines using NLTK’s VADER
- Aggregates daily sentiment scores for each ticker
- Merges news data with historical stock prices (AAPL, GOOGL)
- Engineers technical indicators: RSI, EMA, MACD, PVT, OBV, etc.
- Trains an **XGBoost Regressor** to predict forward returns
- Uses predictions to simulate profit/loss based on trade sizing
- Visualizes cumulative profit over time

---

## 📂 Files

- `alpaca.ipynb`: Collects and saves raw news headlines from the Alpaca API
- `analysis.ipynb`: Scores sentiment, engineers features, trains the model, and simulates trading results

---

## 🧰 Requirements

```bash
pip install pandas numpy plotly ta xgboost scikit-learn nltk python-dotenv
```

Also:
- Get a **free API key** from [Alpaca](https://alpaca.markets/)
- Make sure to set up a `.env` file containing your Alpaca credentials

---

## 📈 Usage

1. Run `alpaca.ipynb` to fetch financial news and store in CSV format
2. Run `analysis.ipynb` to:
   - Load the news and historical stock price data
   - Score headlines with sentiment
   - Compute technical indicators
   - Train the XGBoost regression model
   - Simulate trading and compute profit

---

## 📊 Example Results

- Profit over 1.5 years: **$953.45** from an initial $4,000
- Total Return: **+23.8%**
- Annual Percentage Yield (APY): **15.8%**
- Outperforms typical portfolio manager APYs (~5%)

---

## 🤝 Contributors

- Itay Akad  
- Gilad Bejerano  
- Nir Oren