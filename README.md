# 📈 Stock Price Prediction using LSTM

This project implements a **Long Short-Term Memory (LSTM)** neural network to predict stock prices based on historical stock market data. The model is trained on open prices over a rolling window and is designed to capture temporal dependencies in stock trends using deep learning.

---

## 🚀 Project Highlights

- Built a **deep learning pipeline** using LSTM for univariate time series forecasting.
- Preprocessed and scaled stock market data using **MinMaxScaler**.
- Engineered time-based features to convert raw data into sequences suitable for LSTM input.
- Achieved effective prediction of future stock opening prices based on prior 60-day trends.
- Visualized training and prediction results to evaluate model performance.

---

## 🧠 Technologies Used

- **Python**, **NumPy**, **Pandas**
- **Matplotlib** for visualization
- **Keras** (TensorFlow backend) for building and training the LSTM model
- **scikit-learn** for data preprocessing

---

## 📂 Dataset

- `Price_train.csv` — historical stock data used for training  
- `Price_test.csv` — used for evaluating and testing the model  
- Only the **'Open'** price column is used for univariate prediction

---

## 🔍 Model Architecture

The LSTM model is structured as:

- Input layer: LSTM (50 units) + Dropout
- Hidden layers: LSTM (50 units) + Dropout (2 layers)
- Output layer: Dense (1 unit)

The model is trained using `mean_squared_error` as the loss function and `adam` optimizer.

---

## ⚙️ How It Works

1. The last 60 days of open prices are used to predict the 61st day's price.
2. Data is reshaped to 3D format to fit LSTM input: **(batch_size, time_steps, input_dim)**
3. The model learns temporal relationships in the sequence to predict future values.

---

## 📉 Output

- Predicts next-day stock open prices based on prior 60 days.
- Visualizations show predicted vs actual performance on test data.

---

