# ARIMA vs. Prophet: Performance Comparison

This project aims to compare the performance of two popular time series forecasting models, **ARIMA** and **Prophet**, based on their predictive accuracy and statistical metrics. The results highlight the strengths and weaknesses of each model when applied to a specific dataset.

## **Set Up**

### **Build Environment**
```bash
python -m venv env
```

### **Install Virtual Environment**
```bash
pip install -r requirements.txt
```

### **Activate Virtual Environment**
#### **Windows**
```bash
.\env\Scripts\Activate
```
#### **Linux**
```bash
source env/bin/activate
```

### **Deactivate Virtual Environment**
```bash
deactivate
```

### **Fix Can't Activate Virtual Environment**
Run PowerShell as Administrator and execute:
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

---

## **Models Overview**

### **1. ARIMA (AutoRegressive Integrated Moving Average)**
ARIMA is a statistical model widely used for time series forecasting. It captures the autocorrelations within data to make predictions.

- **Performance Metrics:**
  - **Mean Squared Error (MSE):** 73.62 (lower values indicate better performance)
  - **R-Squared:** 0.227 (closer to 1 indicates better predictive accuracy)
- **Key Insight:**
  - ARIMA demonstrates superior accuracy in forecasting values that are closer to the actual data.

### **2. Prophet**
Prophet is an open-source tool developed by Facebook, designed for forecasting time series data that exhibits strong seasonal patterns.

- **Performance Metrics:**
  - **Mean Absolute Error (MAE):** 0.21 (lower values indicate better performance)
  - **R-Squared:** -5.48 (negative values indicate performance below the baseline)
- **Key Insight:**
  - Prophet shows limitations in handling the given dataset, as evidenced by the negative R-Squared value.

---

## **Comparison Summary**

| Metric                | ARIMA   | Prophet |
|-----------------------|---------|---------|
| Mean Squared Error    | **73.62** | -       |
| Mean Absolute Error   | -       | **0.21** |
| R-Squared             | **0.227** | -5.48   |

- **ARIMA** outperforms Prophet with significantly better MSE and a positive R-Squared, indicating more reliable predictions.
- **Prophet** exhibits lower MAE but fails to achieve a competitive R-Squared score, highlighting its struggle to fit the dataset effectively.

---

## **Conclusion**

Based on the performance metrics:
- **ARIMA** is the better-performing model, offering more reliable and accurate predictions for the dataset.
- **Prophet**, while useful for seasonal data, is less effective in this particular case.

This project underscores the importance of selecting the appropriate model based on the dataset and forecasting requirements.

---

## **Acknowledgments**
- The ARIMA model was implemented using the statsmodels library.
- Prophet was implemented using Facebook's fbprophet package.
- Special thanks to the contributors for their work in developing these forecasting tools.