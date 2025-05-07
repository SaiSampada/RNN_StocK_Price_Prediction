# Stock Price Prediction - Amazon (AMZN)

## Objective
The goal of this project is to predict the closing stock price of Amazon (AMZN) using historical data from 2006 to 2018. We use Recurrent Neural Networks (RNNs) and Long Short-Term Memory (LSTM) models for time series forecasting.

## Dataset
- File: `AMZN_stock_data.csv`
- Total records: 3019
- Columns: `Date`, `Open`, `High`, `Low`, `Close`, `Volume`, `Name`

## Models Used
Trained and tested the following models:

1. Simple RNN
2. RNN with Hyperband Tuning
3. Simple LSTM
4. LSTM with Hyperband Tuning

## Results

| Model                   | Mean Squared Error (MSE) | R² Score |
|------------------------|--------------------------|----------|
| Simple RNN             | 0.0085                   | 0.9305   |
| RNN with Hyperband     | 0.0194                   | 0.8417   |
| Simple LSTM            | 0.0096                   | 0.9213   |
| LSTM with Hyperband    | 0.1387                   | -0.1335  |

**Best Model:** Simple RNN

## Conclusion
Among all the models tested, the Simple RNN performed the best, achieving the lowest Mean Squared Error and the highest R² score. Although LSTM models are generally well-suited for time series tasks, in this case the Simple RNN was more effective. Hyperparameter tuning with Hyperband did not improve performance and in the case of the LSTM model, it significantly worsened the results—likely due to overfitting or poor parameter combinations.


