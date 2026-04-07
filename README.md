## 📈 Netflix Stock Price Forecasting: A Hybrid ML Approach

## 🎯 Project Overview

This project predicts Netflix (NFLX) stock prices by combining the strengths of Deep Learning and Gradient Boosting. By using a Hybrid Ensemble Model, we captured both long-term temporal dependencies and short-term technical momentum.

## 🚀 Performance Highlights

MAPE Accuracy: 94.02% ✅

R-Squared ($R^2$): 0.915 📈

ROC AUC Score: 0.88 🎯

## 🛠️ The Architecture: "The Best of Both Worlds"

To achieve high accuracy, I implemented a Stacked Hybrid Model:

1. LSTM (Long Short-Term Memory): Handles the "Sequential Memory." It looks at the last 60 days of price action to understand the "rhythm" of the market.
2. XGBoost (Extreme Gradient Boosting): Handles the "Technical Signals." It processes engineered features like RSI and Moving Averages to react to sudden volatility.
3. Ensemble Weighting: The final prediction is a weighted average ($70\%$ XGBoost + $30\%$ LSTM), balancing stability with reactivity.

## 🧪 Feature Engineering (Market Signals)

Raw data isn't enough for 94% accuracy. I engineered the following "Alpha" signals:

RSI (Relative Strength Index): 14-day momentum oscillator to identify overbought/oversold conditions.

MA_7 & MA_20: Moving averages to identify short-term and medium-term trend crossovers.

Daily Returns: Measures volatility and percentage change.

Lag Features: Provides the model with "Yesterday's" context to predict "Tomorrow."

## 📊 Visual Insights
1. Correlation HeatmapIdentified which technical indicators had the strongest relationship with the Close price.

2. Actual vs. PredictedVisualized the hybrid model's ability to track Netflix's price movements and sharp rallies.

3. ROC CurveProved the model's directional reliability with an AUC of 0.88, making it a strong tool for "Buy/Sell" decision support.

## 📂 Project Structure

Bash

├── data/

│   └── NFLX.csv           # Historical Netflix Stock Data

├── notebooks/

│   └── EDA_and_Model.ipynb # Full pipeline: Cleaning, EDA, and Hybrid Training

├── models/

│   ├── lstm_model.h5      # Saved Deep Learning Model

│   └── xgb_model.pkl      # Saved XGBoost Regressor

├── README.md              # Project Documentation

└── requirements.txt       # Necessary Libraries

## ⚙️ How to Run

Clone the Repo:

Bash

git clone https://github.com/your-username/netflix-stock-prediction.git

Install Dependencies:

Bash

pip install -r requirements.txt

Run the Notebook: Open EDA_and_Model.ipynb and run all cells to reproduce the 94% accuracy results.

## 🔮 Future Roadmap (The 97% Accuracy Plan)

[ ] Sentiment Analysis: Integrate Twitter/X and News Headlines for "Hype-driven" price moves.

[ ] Hyperparameter Tuning: Implement Bayesian Optimization for the LSTM layers.

[] Macro-Economic Features: Add Interest Rates and Competitor (Disney/Hulu) performance.

## 🤝 ContributingFeel free to fork this project and submit a Pull Request. Let's build a better bot together! 

## 🤖✨Disclaimer: This project is for educational purposes only. 

### Do not use this model as financial advice for actual trading.
