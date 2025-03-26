# Microsoft Stock Price Prediction using LSTM

This project demonstrates the use of a Long Short-Term Memory (LSTM) model to predict the stock prices of Microsoft based on historical data. The dataset used contains the historical stock prices, including open, close, and volume data for the Microsoft stock.

## Dependencies

The following libraries are required to run this project:

- `keras`
- `tensorflow`
- `pandas`
- `numpy`
- `sklearn`
- `matplotlib`
- `seaborn`


## Dataset

The dataset used in this project is a CSV file named `MicrosoftStock.csv`, which contains historical stock prices of Microsoft. The file should include the following columns:

- `date`: The date of the stock record
- `open`: The stock price at market open
- `close`: The stock price at market close
- `volume`: The trading volume of the stock

## Project Overview
1. Data Preprocessing
Data is loaded and visualized, focusing on key features like open, close, and volume.

A sliding window approach is used to create sequences of the last 60 days' stock prices to predict the next day's closing price.

2. Model
A sequential LSTM (Long Short-Term Memory) model is built using Keras. The architecture includes:

Two LSTM layers

A dense layer with ReLU activation

A dropout layer for regularization

A final output layer to predict the next stock price

3. Training
The model is trained on the training data (95% of the dataset) using the Adam optimizer and Mean Absolute Error (MAE) as the loss function. The training process lasts for 20 epochs.

4. Prediction and Visualization
The trained model is used to predict the stock prices on the test dataset (the remaining 5%). The predictions are then visualized alongside the actual test data.

5. Results
The results are visualized using Matplotlib to plot:

Actual stock prices for both training and test datasets.

Predicted stock prices on the test dataset.

## Conclusion:
This project showcases how machine learning, specifically LSTM models, can be used to predict stock prices based on historical data. The accuracy of the model can be further improved with more data and advanced tuning techniques.
