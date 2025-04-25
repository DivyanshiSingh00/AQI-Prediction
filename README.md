
# Air Quality Prediction using ARIMA and LSTM

This project focuses on time series forecasting of Air Quality Index (AQI) using classical statistical models like ARIMA and deep learning-based LSTM models. The aim is to build robust models capable of capturing both seasonal patterns and long-term dependencies in AQI data to generate accurate future forecasts.

---

## 🧠 Objective

- Investigate air quality trends over time using time series analysis.
- Build and compare classical (ARIMA) and deep learning (LSTM) models for AQI forecasting.
- Evaluate and visualize model performance.

---

## 📊 Dataset

- **Source:** Government or public repository of air quality data (e.g., CPCB, Kaggle).
- **Features:** Date, City, AQI.
- **Time Frame:** Yearwise data from 2015 to 2019.

### 📌 Preprocessing Steps:

- Handled missing values using forward-fill and interpolation.
- Performed time series resampling to ensure consistent intervals.
- Applied differencing to remove trends and seasonality.
- Normalized the data for LSTM using MinMaxScaler.

---

## 🧪 Time Series Modeling

### 🔷 ARIMA Model

- **Model Used:** ARIMA(p,d,q)
- **Why Chosen:** Suitable for stationary time series data.
- **Diagnostics:** Residuals checked via ACF/PACF plots and stationarity tests.

### 🔶 LSTM Model

- **Model Used:** LSTM with the following architecture:
  -  **Architecture:**
      - Hidden Size: 32
      - Layers: 2
      - Dropout: 0.3
      - Output Size: 1
      - Optimizer: Adam
- **Why Chosen:** Effective for learning long-term temporal dependencies in data.
- **Diagnostics:** Actual vs Predicted AQI is plotted to check for correctness of the model.

### 📈 Forecast Evaluation

- **Metrics Used:**
  - RMSE (Root Mean Squared Error)
  - MAE (Mean Absolute Error)
  - R² Score

---

## 📉 Results Summary

- ARIMA:
```bash
RMSE  : 39.35
MAE   : 27.86
R²    : 0.66
```
- LSTM:
```bash
RMSE  : 33.81
MAE   : 23.68
R²    :  0.86
```
- The ARIMA model performed well but with low RMSE.
- The LSTM model captured complex temporal structures and showed comparable performance.
- Overall, the hybrid deep learning and statistical approach provided strong forecasting accuracy.

---

## 🚀 Getting Started

### 🧾 Prerequisites

- Python ≥ 3.7
- Jupyter Notebook
- Install required libraries:
```bash
pip install -r requirements.txt
```

### ⚙️ Running the Project

1. **Clone or Fork the Repository**
   - Go to the top-right corner of the GitHub repository and click `Fork`.
   - Clone it to your system:
   ```bash
   git clone https://github.com/your-username/Air-Quality-Prediction.git
   cd Air-Quality-Prediction
   ```

2. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```
3. Open `air_quality.ipynb` and run the cells step-by-step to train ARIMA and LSTM models and generate forecasts.

---

## 📎 Project Structure

```
Air-Quality-Prediction/
│
├── air_quality.ipynb              # Main notebook
├── data/                          # Folder for input CSV files
├── models/                        # Saved model files (ARIMA/LSTM)
├── images/                        # Plots and forecast visualizations
├── requirements.txt               # Required Python packages
└── README.md                      # Project documentation
```

---

## 🤝 Contributing

If you'd like to contribute or suggest improvements, feel free to create a pull request or open an issue.

---

## 📧 Contact

For any questions or feedback, reach out at: **divyanshisingh2885@gmail.com**

---

## 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
