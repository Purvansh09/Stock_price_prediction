# Stock_price_prediction
We will make a model that best predicts the price of a stock
Simple Stock Price Predictor 📈
A beginner-friendly machine learning project that predicts the next day's stock closing price using a simple Linear Regression model.

This project fetches historical stock data, trains a model to learn the relationship between the current day's price and the next day's price, and then makes a prediction.

Table of Contents
Features

Technologies Used

Installation & Usage

How It Works

Sample Output

Disclaimer

License

Features
Fetches real-time historical stock data from Yahoo Finance.

Uses a Linear Regression model to forecast the next day's price.

Visualizes the model's predictions against actual prices.

Calculates Mean Absolute Error (MAE) and R-squared (R 
2
 ) to evaluate model performance.

Technologies Used
Python 3.x

Pandas: For data manipulation and analysis.

yfinance: To download market data from Yahoo Finance.

Scikit-learn: For building and evaluating the machine learning model.

Matplotlib: For data visualization.

Installation & Usage
Follow these steps to get the project running on your local machine.

1. Clone the repository:

Bash

git clone https://github.com/YOUR_USERNAME/stock-price-predictor.git
cd stock-price-predictor
2. Install the required libraries:

Bash

pip install -r requirements.txt
(Note: You will need to create a requirements.txt file containing the libraries listed under "Technologies Used" or just run pip install pandas yfinance scikit-learn matplotlib)

3. Run the script:
Execute the Python script from your terminal.

Bash

python predict.py
You can change the stock ticker inside the script (e.g., from 'AAPL' to 'GOOGL') to predict prices for different companies.

How It Works
Data Fetching: The script uses the yfinance library to download historical daily stock prices for a specified ticker.

Feature Engineering: The core idea is to use today's closing price as a feature to predict tomorrow's closing price. A Next_Close column is created by shifting the Close price data by one day.

Model Training: The data is split into a training set (80%) and a testing set (20%). A LinearRegression model is trained on the training data to learn the linear relationship between the input feature and the target variable.

Prediction & Evaluation: The trained model is used to make predictions on the test set. The model's accuracy is evaluated, and the results are visualized.

Sample Output
When you run the script, you'll see a terminal output and a plot.

Terminal Output:

Successfully downloaded data for AAPL:
                  Open        High         Low       Close   Adj Close     Volume
Date
2020-01-02   74.059998   75.150002   73.797501   75.087502   73.447495  135480400
...
Model training complete.

Mean Absolute Error (MAE): $2.65
R-squared (R²): 0.99

Last known closing price: $170.03
Predicted price for the next trading day: $170.25
Prediction Plot:
The plot visually compares the actual stock prices (blue dots) with the prices predicted by the model (red line).

⚠️ Disclaimer
This project is for educational purposes only and should not be used as financial advice or for making real investment decisions. Stock market prediction is extremely complex and influenced by numerous factors not included in this simple model.

License
This project is licensed under the MIT License. See the LICENSE file for details.
