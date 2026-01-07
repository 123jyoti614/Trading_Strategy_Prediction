# Trading_Strategy_Prediction

## 🚀 Project Overview
This project analyzes real-time and historical cryptocurrency trade data from the **BitMEX platform** to:

- Identify **bullish or bearish market sentiment**
- Filter trading signals using **XGBoost classification**
- Forecast Bitcoin closing prices using **RNN & LSTM**
- Visualize predicted vs actual trends for strategy evaluation

The goal is to improve decision accuracy beyond rule-based signals by leveraging machine learning on engineered technical indicators.

---

## 📌 Problem Statement
Traditional perceptron models treat each price independently and ignore history.  
However, financial markets are sequential by nature.

We aim to:

1. Increase probability of acting on correct signals  
2. Classify whether a signal should be executed  
3. Predict closing price using temporal models  
4. Compare ML performance with raw signals

---

## 📊 Data Source
- Extracted bucketed trade dataset using **BitMEX API**
- ~8 years cryptocurrency trade history
- Features: technical indicators, market metrics per signal

### Target Variables
- Signal Action → {0: Ignore, 1: Act}
- Closing Price Forecast

---

## 🧠 Methodology

### 1. Feature Engineering
- RSI, Moving Averages, Momentum
- Volatility metrics
- Market indicators

### 2. XGBoost Classifier
- Binary classification on signal reliability
- Hyper-parameter tuning
- Train/Validation split

### 3. Deep Learning Forecast
- RNN network for sequence modeling
- LSTM for long-term dependency
- Weight updates via backprop through time

### 4. Evaluation
- Predicted vs Actual curves
- Classification accuracy
- Business intuition checks

---

## 🛠 Tech Stack Used

| Layer | Tools |
|------|------|
| Language | Python |
| ML | Sklearn, XGBoost |
| DL | RNN, LSTM |
| Data | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Notebook | Google Colab |

> ⚠ Note: Dashboarding planned in Power BI / Redash for deployment phase.

---

## 📁 Repository Structure (Suggested)

```bash
├── data
│   └── trades_bucketed.csv
├── notebooks
│   └── eda_bitmex.ipynb
├── src
│   ├── feature_engineering.py
│   ├── xgboost_model.py
│   └── lstm_forecast.py
├── results
│   └── comparison_plots.png
└── README.md
```

---

## ⚙ How to Run

### 1. Clone Repository
```sql
git clone https://github.com/your-username/Trading-Strategy-Prediction.git
cd Trading-Strategy-Prediction
```

### 2. Install Dependencies
```python
pip install -r requirements.txt
```

### 3. Execute Pipeline
```python
python src/feature_engineering.py
python src/xgboost_model.py
python src/lstm_forecast.py
```

---

## 📈 Results & Insights
- XGBoost filtering improved signal execution probability  
- LSTM captured temporal dependencies absent in classical models  
- Trend alignment observed between predicted and actual prices

---

## 🎯 Key Learnings
- Working with **exchange API data**  
- Handling dirty/volatile financial datasets  
- Intuition on algorithm selection  
- Boosting vs sequential DL difference  
- Visualization for business decisions

---

## 🔮 Future Scope
- Order book depth integration  
- Minute-level streaming  
- Multi-action signals → buy/sell/hold  
- Live dashboard in Power BI / Redash

