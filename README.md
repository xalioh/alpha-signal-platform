# Alpha Signal Research Platform

An end-to-end machine learning pipeline built in Python to engineer, evaluate, and visualize alpha signals from equity market data. This project focuses on predicting short-term stock return directions based on technical indicators and testing model-driven strategies.

---

## Project Goals
- Ingest historical ETF data (SPY, QQQ, IWM)
- Engineer predictive features (SMA, RSI, Bollinger Bands, etc.)
- Train machine learning models to classify next-day returns (up/down)
- Evaluate model confidence and signal effectiveness
- Backtest and compare ML-based strategy against Buy & Hold
- Lay the groundwork for future strategy simulation and deployment

---

## Achievements & Key Metrics
✅ Implemented a Random Forest model to predict directional ETF returns with engineered technical features. 
✅ Shifted from a 1-day to a 3-day holding period, improving trade returns and risk-adjusted performance. 
✅ Outperformed the SPY Buy & Hold benchmark with the following strategy metrics:

```
• CAGR: 50.36%
• Sharpe Ratio: 2.48
• Max Drawdown: -19.17%
• Win Rate: 63.18%
• Avg Return per Trade: 0.43%
```

---

## Features Engineered
- Rolling technical indicators:
  - Simple Moving Averages (SMA)
  - Relative Strength Index (RSI)
  - Bollinger Band Width (BBW)
- Lagged returns and volatility
- Categorical target: `1` for next-day up, `0` for down

---

## First ML Model
- Model: Random Forest Classifier
- Evaluation:
  - Initial accuracy ~48% (baseline)
  - Confidence filtering improves precision but lowers recall
  - Holding period tuning (3-day) improved profitability significantly

---

## Project Structure
```bash
alpha-signal-platform/
├── data/                 # Processed feature data
├── models/               # Saved ML model (joblib)
├── notebooks/
│   ├── dataingestion.ipynb   # Data download and cleaning
│   ├── model_training.ipynb  # Feature engineering and ML pipeline
│   └── backtest.ipynb        # Signal evaluation and strategy returns
├── README.md
├── .gitignore
└── requirements.txt
```

---

##  Next Steps
- Expand to multiple ETFs and ensemble signal modeling
- Introduce dynamic thresholding and position sizing
- Deploy a Streamlit dashboard for interactive research
- Explore advanced ML models (XGBoost, LSTM)

---

## Requirements
```bash
pip install -r requirements.txt
```

---

## Keywords
`quantitative finance` · `alpha signals` · `machine learning` · `stock prediction` · `feature engineering` · `python`

---

## Contributing
PRs welcome! This project is under active development.

---

## License
MIT License
