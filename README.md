# Gold Price Prediction with LSTM and BiLSTM

This repository contains a machine learning project that aims to predict gold prices using Long Short Term Memory (LSTM) and Bidirectional Long Short Term Memory (BiLSTM) neural networks. The project utilizes historical gold price data sourced from **Yahoo Finance**, spanning from 2019 to 2023. The results of this project are the performance values of the LSTM and Bi-LSTM models using **R-squared**, **RMSE**, and **MAPE** in gold price prediction.

## Data Collection
The gold price dataset used in this project was collected using the Yahoo Finance API. The data retrieval process was performed with the following parameters:

Symbol: "GC=F" (Gold Futures)
Start Date: January 1, 2019
End Date: July 19, 2023
The choice of the Gold Futures symbol ("GC=F") allows for the extraction of historical gold price data. The dataset spans from the beginning of 2019 to mid-July 2023, providing a substantial timeframe for training and evaluating the LSTM and Bi-LSTM models.

## Model Training
The LSTM (Long Short-Term Memory) and Bi-LSTM (Bidirectional LSTM) models were employed to predict future gold prices based on historical data. The training process involved the following key steps:
### Model Architectures
LSTM Model

The LSTM model architecture consists of an LSTM layer with 50 units, followed by a Dense layer with 25 units and another Dense layer with a single output unit. The model was compiled using the Mean Squared Error (MSE) loss function and the Adam optimizer.

Bi-LSTM Model

The Bi-LSTM model incorporates bidirectional processing for enhanced sequence learning. It consists of a Bidirectional LSTM layer with 50 units, followed by a Dense layer with 25 units, and a final Dense layer with a single output unit. Similar to the LSTM model, the Bi-LSTM model was compiled using the MSE loss function and the Adam optimizer.

### Training Process
The models were trained on preprocessed data using a sliding window approach. For each time step, the model was provided with historical data to predict the subsequent gold price. The training data consisted of 80% of the total dataset, and the remaining 20% was reserved for testing and evaluation, followed by 1 Epoch (You can customize this by using more Epoch because this Epoch is just a sample) Note: I'm using 100 Epoch for a real project.

## Model Visualization
The project includes visualization of the model predictions against the actual gold prices for five different trials. Line graphs were generated to illustrate the predicted values from the LSTM and Bi-LSTM models and the actual gold prices for each trial.

## Results
1. The LSTM model consistently outperformed the Bi-LSTM model across all trials.
2. Trial 5 for the LSTM model exhibited the lowest RMSE, indicating better predictive accuracy.
3. The R-squared values for both models suggest a high degree of correlation between predicted and actual values.
4. The Bi-LSTM model, while slightly less accurate, still demonstrated robust performance in predicting gold prices.

These results provide valuable insights into the predictive capabilities of the LSTM and Bi-LSTM models, guiding further refinements and potential applications in forecasting gold prices.
