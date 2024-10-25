# Tesla Stock Price Prediction Using XGBoost
## Project Overview
This project focuses on building a predictive model for Tesla's stock closing price using historical data. The model employs the XGBoost regression algorithm, a powerful machine learning model that provides robust predictions for time-series data.

## Steps and Methodology
#### 1. Data Loading and Preparation
Loading Data: The Tesla stock data (TSLA.csv) is loaded into a Pandas DataFrame. The columns are renamed for ease of access, and the date column is converted to a datetime format.
Data Visualization: The closing prices are plotted over time using Plotly Express to visualize the trend.
#### 2. Data Scaling and Splitting
Min-Max Scaling: The closing price data is scaled to a range of 0 to 1 using MinMaxScaler to normalize the values, preparing them for model training.
Train-Test Split: The dataset is split into training (70%) and testing (30%) sets to validate the model’s performance.
#### 3. Creating Sequences for Time-Series Forecasting
A function create_dataset is used to create time-step sequences from the dataset, which enables the model to predict future values based on past data points.
Sequence Length: A time step of 15 is chosen, meaning the model uses the past 15 days' data to predict the next day's closing price.
#### 4. Model Training
XGBoost Model: The XGBoost regression model is used with 1000 estimators to fit the training data.
Training Performance: The model is trained on the sequences generated from the training data.
#### 5. Model Evaluation
Performance Metrics: The model's performance is evaluated using:
Mean Absolute Error (MAE): Measures the average absolute errors between predicted and actual values. The MAE achieved is 0.3918.
Root Mean Squared Error (RMSE): Measures the square root of the average of squared differences between predicted and actual values. The RMSE achieved is 0.4691.
## Key Learnings
#### 1. Data Preprocessing
Data scaling using Min-Max normalization was crucial to ensuring that all features were on a similar scale, improving model performance.
#### 2. Time-Series Modeling
Creating sequences using the past time steps allowed the model to effectively learn from the historical data.
#### 3. Model Tuning
Hyperparameter tuning, such as adjusting the number of estimators, played a role in improving the model's prediction accuracy.
#### 4. Performance Evaluation
Using MAE and RMSE provided clear indicators of the model's effectiveness, helping identify areas for potential optimization.
## Conclusion
The XGBoost model provided accurate predictions of Tesla’s stock prices with low errors, demonstrating its effectiveness for time-series forecasting tasks. Further improvements could include experimenting with other models like LSTM or combining models for even better performance.

## Tools and Libraries Used

Pandas and NumPy: For data manipulation and preparation.

Plotly and Matplotlib: For data visualization.

Scikit-learn: For scaling, splitting data, and evaluation metrics.

XGBoost: For building and training the regression model.
