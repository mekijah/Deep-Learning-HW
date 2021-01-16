# LSTM Stock Predictor

![deep-learning.jpg](Images/deep-learning.jpg)

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. You have been asked to help build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.


## Instructions

### Prepare the data for training and testing

Use the starter code as a guide to create a Jupyter Notebook for each RNN. The starter code contains a function to create the window of time for the data in each dataset.

For the Fear and Greed model, you will use the FNG values to try and predict the closing price. A function is provided in the notebook to help with this.

For the closing price model, you will use previous closing prices to try and predict the next closing price. A function is provided in the notebook to help with this.

Each model will need to use 70% of the data for training and 30% of the data for testing.

Apply a MinMaxScaler to the X and y values to scale the data for the model.

Finally, reshape the X_train and X_test values to fit the model's requirement of samples, time steps, and features. (*example:* `X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1))`)

## Results

### Which model has a lower loss?
The model for predicting price using closing prices had the lower loss mean squared error of 0.0570 compared to 0.1242 from the sentiment based model
### Which model tracks the actual values better over time?
The model for predicting price using closing prices tracks better the values over time, as can be seen in the graphs

### closing prices model graph, Predicted vs Real
![real vs predict.jpg](Images/real vs predict.jpg)

### Greed and fear model graph, Predicted vs Real
![greed vs fear.jpg](Images/greed vs fear.jpg)


> Which window size works best for the model?
### The Greed and Fear model with a window of 1 results in lower values for loss function, hence works best for the models

### Greed and fear model loss vs window

loss = 0.0668 / window = 1

loss = 0.0719 / window = 2

loss = 0.0679 / window = 10

### closing prices model loss vs window

loss = 0.0581 / window = 1

loss = 0.0507 / window = 2

loss = 0.0352 / window = 10

- - -

