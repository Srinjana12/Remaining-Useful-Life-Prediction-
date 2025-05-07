# Remaining-Useful-Life-Prediction-

This project demonstrates a complete machine learning pipeline for predicting the Remaining Useful Life (RUL) of turbofan engines using the NASA CMAPSS FD001 dataset. It covers everything from data preprocessing and sequence generation to model training and evaluation using an advanced LSTM-based deep learning architecture.

# Project Highlights
Dataset Used: NASA CMAPSS FD001 (condition-monitoring data from simulated turbofan engines)

# Problem Solved: 
Predict Remaining Useful Life (RUL) at any engine cycle

# Approach:

Time-series windowing of multivariate sensor data

Early RUL clipping for realistic degradation modeling

Train/test split by engine ID

Scaled input features and sequence modeling

# Model: 
Deep LSTM network with dropout, batch normalization, and sequence inputs

# Evaluation Metrics: 
MSE, MAE, and R² on both training and testing sets

# Performance Tracking: 
Includes visual plots of loss curves and predicted vs. actual RUL

# Methodology
# 1. Data Preprocessing
Engine-wise time-series data parsed and RUL calculated

Irrelevant and non-informative sensors removed

Applied MinMaxScaler and StandardScaler to normalize input features

# 2. Sequence Generation
Created overlapping input sequences using a sliding window approach

Early RUL limits applied to avoid unrealistic long-lifespan predictions

Custom utility functions to generate both training and last-cycle test sequences

# 3. Model Architecture
Multi-layer LSTM

Regularization via Dropout and Batch Normalization

Dense output layer with a single neuron for RUL regression

# 4. Model Training & Evaluation
Trained with Mean Squared Error loss and Adam optimizer

EarlyStopping used for better generalization

Evaluation done only on the last cycle of each engine to simulate real-world use cases

# 5: Flask API Deployment
Deployed the LSTM model using a Flask-based REST API.

API accepts JSON input with recent time-series sensor values.

Returns predicted RUL in real time.

Includes Swagger/OpenAPI documentation and Postman test cases.

# Technologies Used
Python, NumPy, Pandas

TensorFlow/Keras (LSTM)

Scikit-learn (Preprocessing + Evaluation)

Matplotlib (Visualization)

Flask (Model Serving)

Swagger & Postman (API Testing)

