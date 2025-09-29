# Trading Guide App

A comprehensive Streamlit application for stock analysis, price prediction, and financial modeling. This application provides traders and investors with essential tools for making informed investment decisions through technical analysis, predictive modeling, and risk assessment.

---

## Live Demo

**Try the app now**: https://stock-analysis-forecasting-time-series-analysis-python-f5ymx3l.streamlit.app/

---

## Deployment

This app is designed to run on Streamlit Cloud.

## Features

### 1. Stock Analysis
- **Real-time Stock Information**: Access detailed company information including business summary, sector, employee count, and website
- **Financial Metrics**: View key financial ratios including Market Cap, Beta, EPS, PE Ratio, Quick Ratio, Revenue per Share, Profit Margins, Debt to Equity, and Return on Equity
- **Interactive Charts**: Candlestick and line charts with multiple time periods (5D, 1M, 6M, YTD, 1Y, 5Y, MAX)
- **Technical Indicators**: RSI, MACD, and Moving Averages for comprehensive technical analysis
- **Historical Data**: Last 10 days of trading data with daily change metrics

### 2. Stock Price Prediction
- **30-Day Forecasting**: Advanced time series forecasting using ARIMA models
- **Data Processing**: Automated data preprocessing including rolling averages, differencing, and scaling
- **Model Validation**: RMSE scoring for model performance evaluation
- **Interactive Visualization**: Plotly charts showing historical data and future predictions
- **Error Handling**: Robust validation for insufficient data and invalid tickers

### 3. CAPM Return Analysis
- **Multi-Stock Analysis**: Compare up to 4 stocks simultaneously
- **Beta Calculation**: Automated beta calculation against S&P 500 benchmark
- **Expected Return**: CAPM-based return calculations for portfolio optimization
- **Data Visualization**: Interactive plots showing normalized and actual stock prices
- **Historical Analysis**: Customizable time periods from 1 to 10 years

### 4. CAPM Beta Calculator
- **Individual Stock Analysis**: Detailed beta and return calculations for single stocks
- **Scatter Plot Analysis**: Visual representation of stock vs market correlation
- **Expected Return Line**: Regression line showing expected returns based on market movements
- **Risk Assessment**: Beta values for measuring systematic risk

## Technical Implementation

### Data Sources
- **Yahoo Finance API**: Real-time and historical stock data via yfinance library
- **FRED API**: S&P 500 data for market benchmark calculations
- **Data Validation**: Comprehensive error handling for API failures and invalid inputs

### Machine Learning Models
- **ARIMA Models**: Autoregressive Integrated Moving Average for time series forecasting
- **Stationarity Testing**: Augmented Dickey-Fuller test for data preprocessing
- **Model Evaluation**: RMSE and R-squared metrics for performance assessment
- **Feature Engineering**: Rolling averages, differencing, and scaling transformations

### Visualization
- **Plotly Integration**: Interactive charts with zoom, pan, and hover capabilities
- **Multiple Chart Types**: Candlestick, line charts, scatter plots, and tables
- **Responsive Design**: Charts adapt to container width for optimal viewing
- **Technical Indicators**: RSI, MACD, and Moving Average overlays

## Installation

### Prerequisites
- Python 3.9 or higher
- pip package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Stock-Analysis-Forecasting-Time-Series-Analysis-Python
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   streamlit run Trading_App.py
   ```

### Dependencies
- streamlit >= 1.28.0
- pandas >= 1.5.0
- yfinance >= 0.2.0
- plotly >= 5.15.0
- numpy >= 1.24.0
- scikit-learn >= 1.3.0
- ta >= 0.10.2
- matplotlib >= 3.6.0
- scipy >= 1.10.0
- statsmodels >= 0.14.0
- pandas-datareader >= 0.10.0

## Usage Guide

### Stock Analysis
1. Navigate to the Stock Analysis page
2. Enter a valid stock ticker symbol (e.g., AAPL, TSLA, MSFT)
3. Select start and end dates for historical analysis
4. Choose chart type (Candlestick or Line) and technical indicators
5. Use time period buttons for quick date range selection

### Stock Prediction
1. Go to the Stock Prediction page
2. Enter a stock ticker symbol
3. Click "Generate Prediction" to start the forecasting process
4. View the 30-day forecast table and interactive chart
5. Review model RMSE score for prediction accuracy

### CAPM Analysis
1. **Multi-Stock CAPM**: Select up to 4 stocks and analysis period, view beta values and expected returns
2. **Individual CAPM**: Choose a single stock for detailed beta calculation and scatter plot analysis

## Project Structure

```
├── Trading_App.py              # Main application entry point
├── pages/
│   ├── Stock_Analysis.py       # Stock information and technical analysis
│   ├── Stock_Prediction.py     # Time series forecasting
│   ├── CAPM_Return.py         # Multi-stock CAPM analysis
│   ├── CAPM_Beta.py           # Individual stock beta calculation
│   └── utils/
│       ├── model_train.py      # Machine learning model functions
│       ├── capm_functions.py   # CAPM calculation utilities
│       └── plotly_figure.py    # Chart generation functions
├── requirements.txt            # Python dependencies
├── setup.py                   # Package setup configuration
└── README.md                  # Project documentation
```

## Deployment

### Streamlit Cloud
This application is optimized for deployment on Streamlit Cloud:

1. Fork this repository to your GitHub account
2. Connect your GitHub account to Streamlit Cloud
3. Deploy directly from the repository
4. The app will automatically install dependencies from requirements.txt

### Local Development
For local development and testing:
```bash
streamlit run Trading_App.py --server.port 8501
```

## Model Performance and Limitations

### Prediction Accuracy
- Models are trained on historical data and may not predict future market conditions
- RMSE scores are provided for transparency in model performance
- Predictions should be used as guidance, not definitive investment advice

### Data Limitations
- Requires minimum 50 days of historical data for predictions
- Market holidays and weekends may affect data availability
- Real-time data depends on Yahoo Finance API availability

### Risk Disclaimers
- All predictions and analyses are for educational purposes only
- Past performance does not guarantee future results
- Users should conduct their own research before making investment decisions
- The application does not provide personalized investment advice

## Contributing

Contributions are welcome! Please follow these guidelines:
1. Fork the repository
2. Create a feature branch
3. Follow PEP 8 coding standards
4. Add appropriate tests for new functionality
5. Update documentation as needed
6. Submit a pull request


