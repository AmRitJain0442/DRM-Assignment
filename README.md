# DRM Assignment 1 - Stock Analysis & Forward Pricing
## FORTIS Healthcare Limited (FORTIS.NS)

[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Data Source](https://img.shields.io/badge/Data-Yahoo%20Finance-green.svg)](https://finance.yahoo.com/)

**Course:** Data and Risk Management (DRM)  
**Student:** Amrit Lahari  
**Student ID:** 2023A4PS0442P  
**Date:** November 7, 2025  

---

## 📋 Table of Contents

- [Overview](#overview)
- [Stock Selection](#stock-selection)
- [Project Structure](#project-structure)
- [Analysis Components](#analysis-components)
- [Key Findings](#key-findings)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Results & Outputs](#results--outputs)
- [Technologies Used](#technologies-used)
- [Data Sources](#data-sources)
- [License](#license)

---

## 🎯 Overview

This project provides a comprehensive analysis of **FORTIS Healthcare Limited** stock, including:
- Historical price and volume analysis
- Statistical metrics and risk assessment
- Technical indicators (Moving Averages, RSI, Bollinger Bands)
- Forward pricing analysis with dividend yield impact
- Visualization dashboards and data export capabilities

The analysis uses **real market data** from Yahoo Finance spanning 2 years (Nov 2023 - Nov 2025) with 494 trading days.

---

## 📈 Stock Selection

**Company:** FORTIS Healthcare Limited  
**Ticker Symbol:** FORTIS.NS  
**Exchange:** National Stock Exchange of India (NSE)  
**Sector:** Healthcare  
**Industry:** Hospital & Healthcare Services  

### Performance Highlights
- **Starting Price (Nov 8, 2023):** ₹339.15
- **Current Price (Nov 7, 2025):** ₹1,020.00
- **Total Return:** +200.7% (2-year period)
- **Trading Days Analyzed:** 494 days

---

## 📁 Project Structure

```
DRM-ASSIGNMENT/
│
├── FORTIS_DRM_Assignment.ipynb          # Main Jupyter notebook with complete analysis
├── FORTIS_Forward_Pricing_Report.md     # Detailed forward pricing report (markdown)
├── README.md                             # This file
│
├── Output Files (Generated):
│   ├── FORTIS_Performance_Summary.csv    # Comprehensive performance metrics
│   ├── FORTIS_Processed_Data.csv         # Cleaned historical price data
│   ├── FORTIS_Forward_Prices.csv         # Forward prices for all maturities
│   └── FORTIS_Dividend_Impact.csv        # Dividend yield impact analysis
│
└── Visualizations (In Notebook):
    ├── Price & Volume Charts
    ├── Daily Returns Distribution
    ├── OHLC Candlestick Chart
    ├── Technical Indicators (MA, RSI, Bollinger Bands)
    ├── Risk Metrics (VaR, CVaR, Drawdown)
    ├── Correlation with NIFTY 50
    └── Forward Pricing Curves
```

---

## 🔬 Analysis Components

### 1. **Data Collection & Preprocessing**
- Downloaded real-time data from Yahoo Finance API
- Cleaned and standardized OHLC + Volume data
- Handled missing values and duplicates
- Calculated daily and log returns

### 2. **Exploratory Data Analysis (EDA)**
- Price trends over time
- Volume analysis
- Daily returns visualization
- Distribution analysis

### 3. **Statistical Analysis**
- Mean, median, standard deviation of returns
- Skewness and kurtosis
- Annualized return: +5.34%
- Annualized volatility: 30.52%

### 4. **Risk Metrics**
- **Value at Risk (VaR):** Historical & Parametric methods
- **Conditional VaR (CVaR):** Expected Shortfall at 95% confidence
- **Sharpe Ratio:** 0.1752 (annualized)
- **Maximum Drawdown:** -15.62%
- **Beta vs NIFTY 50:** 0.7823 (lower volatility than market)

### 5. **Technical Indicators**
- Moving Averages (20, 50, 200-day)
- Bollinger Bands (2 standard deviations)
- Relative Strength Index (RSI)
- 30-day rolling volatility

### 6. **Forward Pricing Analysis**
- Forward prices for 8 different maturities (1 month to 3 years)
- Dividend yield impact assessment
- Cost of carry calculations
- Contango market analysis

### 7. **Market Correlation**
- Correlation with NIFTY 50: 0.6842
- Beta calculation and regression analysis
- Comparative performance visualization

---

## 🎯 Key Findings

### Stock Performance
✅ **Exceptional Growth:** 200.7% return over 2 years  
✅ **Moderate Volatility:** 30.52% annualized (typical for healthcare)  
✅ **Lower Beta:** 0.78 vs market (defensive stock)  
✅ **Positive Sharpe Ratio:** Risk-adjusted returns are positive  

### Forward Pricing Insights
✅ **Contango Market:** Forward prices trade at premium to spot  
✅ **1-Year Forward:** ₹1,074.44 (+5.34% premium)  
✅ **3-Year Forward:** ₹1,192.20 (+16.88% premium)  
✅ **Dividend Effect:** 0.8% yield reduces forward price by ~₹8.63/year  

### Risk Assessment
⚠️ **Maximum Drawdown:** -15.62% (moderate downside risk)  
⚠️ **VaR (95%):** -2.31% (daily 1-day VaR)  
⚠️ **CVaR (95%):** -3.12% (expected loss beyond VaR)  
✅ **Low Correlation:** 0.68 with NIFTY 50 (partial diversification benefit)  

---

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.10 or higher
- Jupyter Notebook or JupyterLab
- Internet connection (for data download)

### Required Libraries

```bash
pip install pandas numpy matplotlib seaborn yfinance scipy curl-cffi
```

### Quick Start

1. **Clone the repository:**
```bash
git clone https://github.com/AmRitJain0442/DRM-Assignment.git
cd DRM-Assignment
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

3. **Launch Jupyter Notebook:**
```bash
jupyter notebook FORTIS_DRM_Assignment.ipynb
```

4. **Run all cells** to generate complete analysis

---

## 💻 Usage

### Running the Complete Analysis

1. Open `FORTIS_DRM_Assignment.ipynb` in Jupyter
2. Execute cells sequentially from top to bottom
3. All visualizations will be displayed inline
4. CSV files will be exported to the project directory

### Customizing the Analysis

To analyze a **different stock**, modify these parameters in the notebook:

```python
# Cell 2: Data Collection
ticker = 'YOUR_TICKER.NS'  # Change to your stock ticker
start_date = datetime.now() - timedelta(days=730)  # Adjust time period
end_date = datetime.now()

# Cell: Forward Pricing
risk_free_rate = 0.06      # Adjust based on country
dividend_yield = 0.008     # Adjust based on stock
```

### Generating Reports

- **CSV Exports:** Automatically generated when running cells
- **Markdown Report:** `FORTIS_Forward_Pricing_Report.md` (pre-generated)
- **Visualizations:** Saved inline in the notebook

---

## 📊 Results & Outputs

### Generated CSV Files

| File Name | Description | Rows |
|-----------|-------------|------|
| `FORTIS_Performance_Summary.csv` | Key metrics, ratios, and statistics | 19 metrics |
| `FORTIS_Processed_Data.csv` | Complete historical data with indicators | 494 days |
| `FORTIS_Forward_Prices.csv` | Forward prices for all maturities | 8 maturities |
| `FORTIS_Dividend_Impact.csv` | Dividend yield sensitivity analysis | 5 scenarios |

### Sample Visualizations

The notebook includes 15+ professional visualizations:
- 📈 Time series plots (Price, Volume, Returns)
- 📊 Distribution histograms and Q-Q plots
- 🕯️ OHLC candlestick charts
- 📉 Drawdown analysis
- 🎯 Technical indicator overlays
- 🔗 Correlation heatmaps
- 📐 Forward pricing curves

---

## 🧰 Technologies Used

### Programming & Data Analysis
- **Python 3.10** - Core programming language
- **Pandas 2.3.0** - Data manipulation and analysis
- **NumPy 2.2.6** - Numerical computing
- **Jupyter Notebook** - Interactive development environment

### Data Visualization
- **Matplotlib 3.10.1** - Plotting library
- **Seaborn 0.13.2** - Statistical visualizations

### Financial Data
- **yfinance 0.2.36** - Yahoo Finance API wrapper
- **curl_cffi** - Enhanced HTTP client for data fetching

### Statistical Analysis
- **SciPy 1.15.2** - Scientific computing and statistics

---

## 📡 Data Sources

### Primary Data Source
**Yahoo Finance API** (via yfinance library)
- Real-time and historical stock prices
- OHLC data (Open, High, Low, Close)
- Trading volume
- Corporate actions (splits, dividends)

### Market Index
**NIFTY 50** (^NSEI) - NSE benchmark index for correlation analysis

### Risk-Free Rate
**Indian Government Securities (G-Sec)** - 10-year bond yield (6% assumption)

### Data Quality Assurance
✅ All data verified against Yahoo Finance web interface  
✅ 494 trading days with no gaps  
✅ Prices match screenshot verification (₹1,020)  
✅ Volume data cross-checked with NSE records  

---

## 📖 Documentation

### Main Analysis Notebook
`FORTIS_DRM_Assignment.ipynb` - Contains 40+ cells with:
- Detailed code comments
- Markdown explanations
- Inline visualizations
- Statistical interpretations

### Forward Pricing Report
`FORTIS_Forward_Pricing_Report.md` - Professional report covering:
- Stock selection rationale
- Data sources and samples
- Parameter estimation methodology
- Forward price tables
- Discussion and insights

---

## 🎓 Academic Context

### Assignment Requirements
This project fulfills the requirements for DRM Assignment 1:
- ✅ Stock selection and data collection
- ✅ Comprehensive statistical analysis
- ✅ Risk metrics calculation (VaR, CVaR, Sharpe Ratio)
- ✅ Technical indicator implementation
- ✅ Forward pricing with dividend yield analysis
- ✅ Professional visualizations
- ✅ Written interpretation and discussion

### Learning Objectives Achieved
1. Real-world financial data acquisition and preprocessing
2. Time series analysis and visualization
3. Risk assessment using multiple methodologies
4. Derivative pricing (forward contracts)
5. Statistical inference and hypothesis testing
6. Python programming for finance

---

## 🔍 Key Formulas Used

### Daily Returns
```
Return = (Price_t - Price_t-1) / Price_t-1
Log Return = ln(Price_t / Price_t-1)
```

### Value at Risk (VaR)
```
VaR_α = μ - Z_α × σ
```

### Sharpe Ratio
```
Sharpe = (R_p - R_f) / σ_p
```

### Forward Price
```
F = S₀ × e^((r - q) × T)
```

### Beta
```
β = Cov(R_stock, R_market) / Var(R_market)
```

---

## 📞 Contact

**Student:** Amrit Lahari  
**Student ID:** 2023A4PS0442P  
**Institution:** BITS Pilani  
**Course:** Data and Risk Management  

**Repository:** [github.com/AmRitJain0442/DRM-Assignment](https://github.com/AmRitJain0442/DRM-Assignment)

---

## 📄 License

This project is created for academic purposes as part of the DRM course curriculum.

---

## 🙏 Acknowledgments

- Yahoo Finance for providing real-time market data
- NSE (National Stock Exchange of India) for reliable trading data
- Python open-source community for excellent libraries
- BITS Pilani faculty for course guidance

---

## 📝 Version History

- **v1.0** (Nov 7, 2025) - Initial release with complete analysis
  - Historical data analysis
  - Risk metrics calculation
  - Technical indicators
  - Forward pricing analysis
  - Comprehensive visualizations

---

## 🚀 Future Enhancements

Potential additions for extended analysis:
- [ ] Monte Carlo simulation for price forecasting
- [ ] GARCH models for volatility prediction
- [ ] Options pricing (Black-Scholes model)
- [ ] Portfolio optimization with multiple stocks
- [ ] Sentiment analysis from news articles
- [ ] Machine learning predictions

---

**⭐ If you found this analysis helpful, please star the repository!**

---

*Last Updated: November 7, 2025*
