Project Overview

This project focuses on time-series forecasting using a Long Short-Term Memory (LSTM) neural network to predict hourly temperature for the next 24 hours based on historical weather data.

The goal of this project is to demonstrate:

Practical time-series preprocessing

Deep learning–based forecasting

Feature engineering for sequential data

A real-world, beginner-friendly data science workflow

 Problem Statement

Given historical hourly weather observations, predict future temperature values while capturing temporal dependencies, trends, and seasonality.

 Dataset

Source: Kaggle – Weather Dataset

Frequency: Hourly

Key Features:

dt_iso (Datetime)

Temperature

Humidity

Pressure

Wind Speed

Cloud and rain indicators

 Data Preprocessing

The following steps were applied to prepare the time-series data:

Converted dt_iso to proper datetime format

Sorted data chronologically

Handled missing values

Extracted time-based features:

Hour

Day

Month

Day of week

Scaled features using MinMaxScaler

Created rolling sequences for LSTM input

 Feature Engineering

Lagged temperature values

Time-based features for seasonality

Sequential windows of past 24 hours as model input

 Model Architecture

Model Type: LSTM (Deep Learning)

Framework: TensorFlow / Keras

Input: Past 24 hours of weather data

Output: Next hour temperature (iterated for 24-hour forecast)

Regularization: Dropout layers

 Model Training

Loss Function: Mean Squared Error (MSE)

Optimizer: Adam

Time-based train-validation split

Training monitored using validation loss

 Evaluation Metrics

Root Mean Squared Error (RMSE)

Mean Absolute Error (MAE)

Training vs Validation loss curves

 Results

The trained LSTM model successfully learns short-term temperature trends and produces reasonable hourly forecasts when provided with sufficient historical data.

This project emphasizes learning and correctness of the pipeline over aggressive optimization.

 Challenges Faced

Datetime handling errors (.dt accessor issues)

Feature mismatch between training and inference

Understanding sequence creation for LSTM

Scaling and inverse scaling confusion

 Key Learnings

Time-series data must never be shuffled

Feature consistency is critical in ML pipelines

LSTM models require careful sequence preparation

Most issues occur during preprocessing, not modeling

Debugging is a core data science skill

 Tools & Technologies

Python

Pandas, NumPy

Scikit-learn

TensorFlow / Keras

Matplotlib

 Future Improvements

Compare LSTM vs GRU models

Multi-step forecasting (48–72 hours)

Multivariate forecasting (temperature + humidity)

Model deployment as a web application
