# GMF Investments: Time Series Forecasting and Portfolio Optimization

## Project Overview

This project was developed as part of a financial analytics assignment for **Guide Me in Finance (GMF) Investments**, a technology-driven financial advisory firm specializing in personalized portfolio management. The objective is to use historical financial market data and time series forecasting techniques to support portfolio management decisions by analyzing three representative financial assets:

- **Tesla (TSLA)** – High-risk, high-growth equity
- **Vanguard Total Bond Market ETF (BND)** – Low-risk bond ETF
- **SPDR S&P 500 ETF (SPY)** – Broad market equity ETF

Rather than attempting to predict exact future stock prices, the project acknowledges the **Efficient Market Hypothesis (EMH)** and uses forecasting models to identify market trends and support investment decision-making as one component of a broader portfolio management framework.

---

## Project Objectives

The project consists of five major tasks:

1. **Data Collection and Exploratory Data Analysis (EDA)**
   - Download historical financial data using YFinance.
   - Clean and preprocess the data.
   - Perform exploratory data analysis.
   - Calculate financial risk metrics.
   - Conduct stationarity testing.

2. **Time Series Forecasting**
   - Build and evaluate ARIMA models.
   - Build and evaluate LSTM deep learning models.
   - Compare forecasting performance using multiple evaluation metrics.

3. **Future Price Forecasting**
   - Generate future stock price forecasts.
   - Produce confidence intervals for forecast uncertainty.

4. **Portfolio Optimization**
   - Apply Modern Portfolio Theory (MPT).
   - Construct the Efficient Frontier.
   - Recommend an optimal asset allocation.

5. **Portfolio Backtesting**
   - Compare the optimized portfolio against a benchmark portfolio consisting of:
     - 60% SPY
     - 40% BND

---

## Project Structure

```
GMF-Time-Series-Forecasting/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── eda.ipynb
│   ├── modeling.ipynb
│   ├── portfolio.ipynb
│   └── backtesting.ipynb
│
│
├── figures/
│
├── requirements.txt
│
└── README.md
```

---

## Technologies Used

- Python 3.11+
- Jupyter Notebook

### Main Libraries

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- statsmodels
- pmdarima
- scikit-learn
- tensorflow / keras
- yfinance

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/semegn19/portfolio-optimization.git

cd portfolio-optimization
```

### 2. Create a Virtual Environment (Recommended)

Windows

```bash
python -m venv venv

venv\Scripts\activate
```

Linux/macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Alternatively, install the required packages manually:

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels pmdarima scikit-learn tensorflow yfinance jupyter
```

---

## Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Run the notebooks in the following order:

1. eda.ipynb
2. modeling.ipynb
3. forecasting.ipynb
4. portfolio.ipynb
5. backtesting.ipynb

Running the notebooks sequentially ensures that processed datasets generated in earlier tasks are available for subsequent analyses.

---

## Data Source

Historical market data is obtained directly from the **Yahoo Finance** database through the **YFinance** Python library.

### Assets Used

| Asset | Ticker | Description |
|--------|--------|-------------|
| Tesla | TSLA | High-growth technology stock |
| Vanguard Total Bond Market ETF | BND | Investment-grade U.S. bond ETF |
| SPDR S&P 500 ETF | SPY | ETF tracking the S&P 500 Index |

### Time Period

**January 1, 2015 – June 30, 2026**

### Variables Collected

- Date
- Open
- High
- Low
- Close
- Adjusted Close
- Volume

---

## Forecasting Models

The project implements and compares two forecasting approaches:

### ARIMA

- Statistical time series forecasting model
- Parameters selected using Auto ARIMA
- Evaluated using:
  - MAE
  - RMSE
  - MAPE

### LSTM

- Deep learning recurrent neural network
- 60-day input sequence
- Two stacked LSTM layers with dropout regularization
- Optimized using the Adam optimizer
- Evaluated using:
  - MAE
  - RMSE
  - MAPE

---

## Portfolio Optimization

The project applies Modern Portfolio Theory to:

- Estimate expected returns
- Calculate portfolio risk
- Generate the Efficient Frontier
- Identify an optimal portfolio allocation
- Compare the optimized portfolio with a benchmark portfolio (60% SPY / 40% BND)

---

## Outputs

The project produces:

- Cleaned financial datasets
- Exploratory data analysis visualizations
- Financial risk metrics
- Stationarity test results
- ARIMA forecasts
- LSTM forecasts
- Model comparison metrics
- Portfolio optimization results
- Efficient Frontier visualization
- Portfolio backtesting performance

---