# Stock Price Predictor Project Description

This project uses a simple machine learning model `RandomForestClassifier` to predict stock price movement (up or down) on the following day using historical data.

The process begins with retrieving data using the `yfinance` library to get historical stock price data for a specified ticker (in my case AAPL for Apple). The dataset includes open, high, low, close, and volume starting from a user-defined date. The predictions are made based on these metrics.

Rolling averages of closing prices over various time horizons are calculated as well as the ratio of current closing prices to these averages. Additionally, trend indicators are created to count the number of upward movements within specific historical windows. This is done to capture trends and patterns, providing the model with the necessary data to make better predictions.

`RandomForestClassifier` is used as the ML model b/c it seemed the most suitable for this project among the simple Ml models, with `random_state=1` for consistent results.

The model is trained on an expanding window of historical data and testing it on unseen data in fixed intervals. This approach ensures that the model is tested in conditions similar to real-world conditions.

The performance of the model is measured using precision, recall, and accuracy metrics. Several dataframes, graphs and bar charts are used for clarity.

I did this project to get a foundation for predictive modeling in financial markets and have an better idea of what techniques hedge funds use.

Future work could expand the project to include additional features such as technical indicators or macroeconomic variables such as inflation rate and tresury bonds yield as well as explore alternative classification algorithms like `Gradient Boosting` or `Neural Network`. Using the model in a real-time environment for live predictions would also be a significant next step too.
