# Stock Price Predictor Project Description

This project uses a simple ML model `RandomForestClassifier` to predict stock price movement (up or down) on the next day

The process begins with fetching data from `yfinance` . Then you clean the data (perhaps not applicable to the new version).

Rolling averages of closing prices over different times are calculated as well as the ratio of current closing prices to these averages. Additionally, the program count the number of upward movements within specific time windows. This is done to capture outliers.

The data is split into training and testing data. The model is trained on a training set and then tested on the testing set.

The performance is measured using precision, recall, and accuracy metrics.

I did this project to get a foundation for modeling in financial markets and have an better idea of what techniques hedge funds use.
