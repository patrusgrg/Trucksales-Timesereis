# Truck Sales Time Series Analysis

A comprehensive case study analyzing monthly truck sales using machine learning and classical time-series forecasting methods.

**Author:** Patrus Gurung

## 📋 Overview

This project analyzes monthly truck sales data from Kaggle's [Dummy Truck Sales for Time Series](https://www.kaggle.com/datasets/ddosad/dummy-truck-sales-for-time-series) dataset. The analysis compares tree-based ensemble models (XGBoost) with classical time-series approaches (ARIMA) to forecast future truck sales and demonstrate practical forecasting techniques.

## 🎯 Project Goals

- Model time series data using **XGBoost**, a tree-based ensemble model
- Construct appropriate **time-based and lag features** for temporal data
- Compare XGBoost performance against **ARIMA**, a classical time-series model
- Evaluate forecasting accuracy on held-out test sets and future predictions
- Demonstrate the business value of accurate sales forecasting

## 📊 Dataset

- **Source:** Kaggle - Dummy Truck Sales for Time Series
- **Format:** CSV (`Truck_sales.csv`)
- **Content:** Monthly truck sales observations with date information
- **Key Statistics:**
  - Mean Sales: ~429 trucks/month
  - Range: 152–958 trucks/month
  - Notable seasonality and mild trend patterns

## 🛠️ Key Features

### Data Preparation
- Convert date strings to proper datetime format
- Sort chronologically and set as index
- Handle missing values

### Feature Engineering
- **Time-based features:** Month, quarter, year, day of week
- **Lag features:** Previous 1, 3, 6, 12-month sales values
- **Rolling statistics:** Moving averages and seasonal decomposition

### Models Implemented
1. **XGBoost Regressor**
   - Tree-based ensemble approach
   - Captures non-linear relationships
   - Efficient handling of feature interactions

2. **ARIMA (AutoRegressive Integrated Moving Average)**
   - Classical statistical time-series model
   - Stationarity testing (ADF test)
   - Automatic parameter selection

### Evaluation Metrics
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Time-series cross-validation with walk-forward approach

## 📚 Notebook Structure

The Jupyter notebook (`TruckTimeseries.ipynb`) is organized into the following sections:

1. **Introduction** – Project overview and goals
2. **Data Loading & Exploration** – Load data, basic statistics, visualizations
3. **Time Series Preparation** – DateTime conversion, sorting, indexing
4. **Train-Test Split** – Chronological 80/20 split preserving temporal order
5. **Feature Engineering** – Create lag and time-based features
6. **Exploratory Analysis** – Visualize trends, seasonality, stationarity
7. **Model Development**
   - XGBoost setup and training
   - ARIMA parameter selection and fitting
8. **Model Evaluation** – Compare performance on test set
9. **Future Forecasting** – Generate predictions beyond observed data
10. **Business Insights** – Discuss practical applications and recommendations

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook or JupyterLab
- Required packages (see below)

### Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/patrusgrg/Trucksales-Timesereis.git
cd Trucksales-Timesereis
pip install -r requirements.txt
```

### Running the Analysis

1. Open the notebook:
```bash
jupyter notebook TruckTimeseries.ipynb
```

2. Run cells sequentially from top to bottom, or:
   - Use Jupyter's "Run All" option to execute the entire analysis
   - Run individual cells to explore specific sections

3. The notebook will automatically download the dataset from Kaggle (requires `kagglehub` authentication)

## 📦 Required Packages

```
pandas
numpy
matplotlib
scikit-learn
xgboost
statsmodels
kagglehub
jupyter
```

Install via:
```bash
pip install pandas numpy matplotlib scikit-learn xgboost statsmodels kagglehub jupyter
```

## 🔑 Key Findings & Insights

- **Seasonality:** Strong annual patterns observed in truck sales
- **Trend:** Mild upward trend with cyclic behavior
- **Model Comparison:** XGBoost vs. ARIMA trade-offs documented
- **Forecasting Horizon:** Model performance evaluated at different forecast lengths
- **Business Impact:** Forecasts enable inventory planning, resource allocation, and demand management

## 📊 Visualizations Included

- Time series plot with trend and seasonality
- Autocorrelation (ACF) and partial autocorrelation (PACF) plots
- Model predictions vs. actual values
- Residual analysis and error distributions
- Forecast uncertainty bands (where applicable)

## 🧪 Model Validation

- **Walk-forward cross-validation** for robust performance assessment
- **Stationarity testing** using Augmented Dickey-Fuller (ADF) test
- **Seasonal decomposition** analysis
- **Holdout test set** evaluation with multiple metrics

## 📈 Use Cases

This analysis demonstrates practical applications for:
- **Inventory Management** – Optimize stock levels based on predicted demand
- **Production Planning** – Schedule manufacturing capacity
- **Financial Forecasting** – Revenue and cash flow projections
- **Resource Allocation** – Workforce planning and scheduling
- **Strategic Planning** – Long-term business decisions

## 🤝 Contributing

Contributions are welcome! Please feel free to:
- Open issues for bugs or improvements
- Submit pull requests with enhancements
- Suggest new features or analyses

## 📝 License

This project is provided as-is for educational and analytical purposes.

## 📧 Contact

For questions or feedback, please reach out to **Patrus Gurung**.

---

**Last Updated:** December 2025
