# StockPredictor
## Description
In this project, I analyzed the stock, Apple Inc. (AAPL), trying to predict the closing stock using Python and Machine Learning (LSTM). Using historical market data from Yahoo Finance and a Long Short-Term Memory (LSTM) neural network, the model learns patterns in price movement, volatility and momentum to forecast future stock trends.

## Analyzing Data
The csv file of AAPL was obtained through Yahoo Finance, where I imported its data using the library'yfinance', and where it was cleaned and converted it into a CSV file for time-series analysis. The dataset includes: Open, High, Low, Close prices, Adjusted Close prices, Trading Volume.


## Building the Model
The model used **Adjusted Close** section as the prediction target, reflecting Apple's true market value over time. The data was scaled using scikit-learn's MinMaxScaler and  transformed into a 60-day time-series window. I implemented a **Keras Sequential** model using a Long Short-Term Memory layer and Dense output layer was implemented to learn trending patterns to forecast the next adjusted close price.

## Training the Model
I split the scaled data into training and test sets and used trial and error to fine-tune key hyperparameters. By experimenting with different batch sizes and number of epochs, I found that using a batch size of 1 and training for 10 epochs produced the most accurate results.

## Result
After training and testing my model with AAPL stock data from 12-Jan-2021 to 09-Jan-2026 (Updated CSV), it predicted that the closing price for AAPL Stock to be $260.36 on 12-Jan-2026. As of the day 12-Jan-2026, it can be concluded that my model was successfully trained to predict AAPL's stock price, with the actual adjusted closing price to be $260.25, which is $0.11 away from the predicted price. The model can also be seen to predict the overall trends of the prices as seen in the graphs.

## References
- https://ca.finance.yahoo.com/quote/AAPL/history/
- https://www.youtube.com/watch?v=QIUxPv5PJOY
