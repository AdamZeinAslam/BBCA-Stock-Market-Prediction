# BBCA Stock Price Prediction using LSTM (Quantitative Data-Driven Approach)

## Overview
This project aims to predict the stock price of **Bank Central Asia (BBCA.JK)** using a **data-driven quantitative approach** with **Long Short-Term Memory (LSTM) neural networks**.

Stock price prediction is a challenging problem due to market volatility and noise. This project applies a **deep learning time-series model** to learn patterns from historical stock data and generate predictions for future prices.

The goal of this project is to demonstrate how **machine learning and deep learning can be applied to financial market data**, which is commonly used in **quantitative trading**.

---

## Dataset
The dataset contains historical stock price data for **BBCA (Bank Central Asia)** from the Indonesian Stock Exchange.

Features included in the dataset:

- **Open** – Opening price
- **High** – Highest price during the trading day
- **Low** – Lowest price during the trading day
- **Close** – Closing price
- **Volume** – Trading volume

Number of observations: **232 trading days**

Example of dataset structure:

| Open | High | Low | Close | Volume |
|-----|-----|-----|-----|-----|
| 7600 | 7675 | 7500 | 7500 | 202433406 |
| 7700 | 7775 | 7625 | 7625 | 170666703 |

---

## Methodology

The workflow of this project follows several steps:

### 1. Data Preprocessing
- Load stock market dataset using **Pandas**
- Clean numeric columns
- Convert dataset into numerical format
- Remove unnecessary columns
- Normalize data using **MinMaxScaler**

Normalization is used to scale the values between **0 and 1**, which improves neural network performance.

---

### 2. Train-Test Split
The dataset is split into:

- **70% training data**
- **30% testing data**

This allows the model to learn from historical data and evaluate performance on unseen data.

---

### 3. Time Series Dataset Construction

A custom function is used to transform the dataset into **supervised learning format** using a sliding window approach.

This allows the LSTM model to learn temporal dependencies in stock price movements.

---

### 4. LSTM Model Architecture

The prediction model uses a **Long Short-Term Memory (LSTM)** neural network implemented with Keras/TensorFlow.

LSTM is chosen because it is well suited for time-series forecasting problems and can capture long-term dependencies in sequential data.

---

### 5. Model Training

The model is trained with the following configuration:

- **Optimizer:** Adam
- **Loss Function:** Mean Squared Error (MSE)
- **Epochs:** 150
- **Batch Size:** 1

The training process minimizes prediction error between predicted and actual stock prices.

---

### 6. Model Evaluation

The model performance is evaluated using **Root Mean Squared Error (RMSE)**.

Results:
- **Train Score: 0.05 RMSE**
- **Test Score: 0.05 RMSE**


A lower RMSE indicates better prediction accuracy.

---

### 7. Visualization

The project also visualizes:

- Predicted vs Actual **training data**
- Predicted vs Actual **testing data**

These plots help evaluate how well the model captures the trend of the stock price.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib

---

## Potential Improvements

Future improvements for this project include:

- Using **more historical data**
- Adding **technical indicators** (RSI, MACD, Moving Average)
- Building a **trading strategy simulation**
- Evaluating model performance with additional metrics

---

## Applications

This project demonstrates how machine learning can be applied in:

- **Quantitative trading**
- **Financial market analysis**
- **Algorithmic trading research**
- **Time-series forecasting**
