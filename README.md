# Stock Price Prediction

This repository contains a Jupyter Notebook project that demonstrates how to predict the next day's closing stock price using historical market data and machine learning.

## Overview

The project uses the **Random Forest Regressor** from `scikit-learn` to forecast the next day's closing price for Apple Inc. (AAPL). It loads historical stock data via the `yfinance` library, structures the feature set and target variable, and evaluates the model's performance using Mean Squared Error (MSE).

## Features

- **Data Fetching:** Automatically downloads AAPL stock data from January 1, 2020, to January 1, 2024, using Yahoo Finance.
- **Data Preprocessing:** Creates the target variable by shifting the close price, handling missing values in the process.
- **Machine Learning:** Utilizes a Random Forest Regressor to model the relationship between the features (Open, High, Low, Volume) and the target (Next Day Close).
- **Time-Series Split:** Correctly splits the data sequentially (80% training, 20% testing) to preserve the temporal order of stock prices.
- **Visualization & Evaluation:** Plots the actual vs. predicted closing prices and calculates the Mean Squared Error (MSE) to evaluate the model.

## Prerequisites

To run this notebook, you will need Python 3 installed along with the following libraries:

- `yfinance`
- `pandas`
- `matplotlib`
- `scikit-learn`

You can install these dependencies using `pip`:

```bash
pip install yfinance pandas matplotlib scikit-learn
```

## Usage

1. Clone this repository to your local machine:
   ```bash
   git clone <your-repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd stock-price-prediction
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook stock_price_prediction.ipynb
   ```
4. Run all the cells in the notebook to download the data, train the model, and view the predictions and visualizations.

## Project Structure

- `stock_price_prediction.ipynb`: The main Jupyter Notebook containing all the code for data loading, preprocessing, model training, and evaluation.
- `README.md`: Project documentation.

## Results

The model visually demonstrates the predicted trend alongside the actual historical stock closing prices. The performance is assessed quantitatively using Mean Squared Error (MSE), which indicates the average squared difference between the estimated values and the actual value.

## Potential Improvements

- Implement more complex models or deep learning architectures (e.g., LSTMs) suited for time constraints.
- Feature engineering: Add technical indicators like Moving Averages, RSI, or MACD to provide the model with better signals.
- Hyperparameter tuning to optimize the Random Forest Regressor.
