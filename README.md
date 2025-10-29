# Sales Forecasting Project

This project performs time series forecasting on Adidas US sales data using multiple approaches, including classical statistical models, machine learning models, and deep learning models. The goal is to predict future sales and compare the performance of different models.

---

## **Dataset**

- Source: `Adidas US Sales Datasets.xlsx`
- Columns used:  
  - `Invoice Date` – date of the invoice  
  - `Total Sales` – total sales amount  
- Data preprocessing steps:  
  - Converted `Invoice Date` to datetime format  
  - Aggregated sales monthly  
  - Handled missing values  

---

## **Forecasting Models**

The project uses the following forecasting techniques:

1. **Moving Average**  
   - 3-month and 6-month moving averages  

2. **ARIMA (AutoRegressive Integrated Moving Average)**  
   - Parameters: (p=1, d=1, q=1)  
   - Captures trend and seasonality  

3. **Holt-Winters / Exponential Smoothing**  
   - Additive trend and seasonal components  
   - Seasonal period = 12 months  

4. **Random Forest (Machine Learning)**  
   - Lag features: 1-month and 2-month lags  
   - Moving averages as additional features  

5. **LSTM (Deep Learning)**  
   - Sequence length: 3 months  
   - Scaled data with MinMaxScaler  
   - One LSTM layer with 50 units and a dense output  

---

## **Evaluation Metrics**

The models are evaluated using:

- **RMSE (Root Mean Squared Error)**  
- **MAE (Mean Absolute Error)**  
- **R² (Coefficient of Determination)**  

| Model            | RMSE           | MAE           | R²         |
|-----------------|---------------|---------------|------------|
| Moving Average  | 8.94e+06      | 7.45e+06      | 0.18       |
| ARIMA           | 1.19e+07      | 9.71e+06      | -0.45      |
| Holt-Winters    | 4.89e+07      | 4.79e+07      | -23.52     |
| Random Forest   | 1.02e+07      | 8.57e+06      | -0.07      |
| LSTM            | 1.07e+07      | 1.02e+07      | -0.18      |

**Conclusion:**  
- Moving Average had the lowest RMSE and best R² among all models.  
- Holt-Winters performed the worst, likely due to insufficient data or high variance.  
- Machine learning and deep learning models performed moderately well.  

---

## **Forecasts**

Example: Forecast for the next month:

- Moving Average: `x`  
- ARIMA: `x`  
- Holt-Winters: `x`  
- Random Forest: `x`  
- LSTM: `x`  

*(Replace `x` with actual forecast values from your notebook.)*

---

## **How to Run**

1. Install required packages:

```bash
pip install pandas numpy matplotlib scikit-learn statsmodels tensorflow openpyxl
