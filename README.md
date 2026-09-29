# Stock Price Forecasting with LSTM

A deep learning project focused on forecasting daily stock closing prices using **Long Short-Term Memory (LSTM)** networks.

The project uses historical data from **GOOGL (Alphabet Inc.)** and **INTC (Intel Corporation)** to evaluate baseline and improved LSTM configurations for time series forecasting.

## Project Description

The goal is to learn temporal patterns from historical closing prices and predict the next trading day's price.

The forecasting process uses a **5-day sliding window** and a **1-day forecasting horizon**, with the final year reserved for testing.

## What I Did

* Prepared and explored historical stock price data from GOOGL and INTC.
* Applied chronological train-test splitting and **RobustScaler** preprocessing.
* Created 5-day sliding-window sequences for next-day prediction.
* Developed and compared **Baseline LSTM** and **Improved LSTM** models.
* Evaluated forecasting performance using **RMSE, MAE, and MAPE**.
* Visualized actual versus predicted stock prices.

## Tools

* **Python** – programming and data analysis.
* **TensorFlow / Keras** – LSTM model development and training.
* **Pandas & NumPy** – data processing and numerical computation.
* **Scikit-learn** – data scaling and evaluation metrics.
* **Matplotlib & Seaborn** – data visualization.

## Insights

The analysis revealed several important findings:

* **Improved LSTM performed better on GOOGL:** RMSE decreased from 34.64 to 28.47, while MAE decreased from 25.09 to 18.28 and MAPE from 1.99% to 1.48%.
* **Baseline LSTM performed better on INTC:** RMSE decreased slightly from 1.56 to 1.60 when using the improved model, while MAE and MAPE also increased slightly.
* **Model performance is dataset-dependent:** the improved configuration benefited GOOGL but did not improve forecasting performance for INTC.
* **Regularization helped address overfitting:** the improved GOOGL model incorporated Dropout, adaptive learning-rate reduction, and EarlyStopping to improve generalization.

## Advice

Based on the findings, the following improvements can be considered:

* Tune the LSTM hyperparameters to find the configuration that provides better forecasting performance for each stock.
* Experiment with different lookback windows, such as 5, 10, or 20 days, to determine how much historical data is useful for prediction.
* Add more stock features such as Open, High, Low, and Volume instead of relying only on the closing price.
* Experiment with different LSTM architectures, such as changing the number of LSTM units or adding additional LSTM layers.

## Repository

```text
├── GOOGL.csv
├── INTC.csv
└── Stock_Prediction_LSTM.ipynb
```
