# 📈 Stock Price Direction Predictor

This project predicts whether a stock's **closing price** will go **up or down** the next day using historical data and machine learning techniques.

##  Project Overview

The model is trained on features engineered from historical stock price data such as:

- Daily returns
- Moving averages (MA5, MA10)
- Volatility
- Relative Strength Index (RSI)

It uses a **Random Forest Classifier** to predict whether the stock's price will **rise (1)** or **fall (0)** the next day.

##  Machine Learning Workflow

1. **Data Collection**  
   Load stock data using `yfinance` (Yahoo Finance).

2. **Feature Engineering**  
   - Daily returns: `df['Return']`
   - Moving Averages (5-day, 10-day)
   - Volatility (5-day rolling standard deviation)
   - RSI (14-day)
   - Target variable: 1 if tomorrow's price is higher than today's, else 0

3. **Model Training**  
   - Model: `RandomForestClassifier`
   - Train-test split: 80% training, 20% testing
   - Evaluation: Accuracy, Confusion Matrix, Classification Report

4. **Visualization & Prediction**  
   - Evaluate model performance
   - Predict direction on new data
   - Optional: Run as a **Streamlit** app for UI interaction



