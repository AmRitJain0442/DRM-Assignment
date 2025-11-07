# Forward Pricing Analysis Report
## FORTIS Healthcare Limited

**Student Name:** Amrit Lahari  
**Student ID:** 2023A4PS0442P  
**Date:** November 7, 2025  
**Assignment:** DRM Assignment 1 - Forward Pricing Analysis

---

## ✓ The Stock You Selected (Name, Ticker)

**Company Name:** FORTIS Healthcare Limited  
**Stock Ticker:** FORTIS.NS  
**Exchange:** NSE (National Stock Exchange of India)  
**Sector:** Healthcare  
**Industry:** Hospital & Healthcare Services  

**Current Market Price:** ₹1,020.00 (as of November 7, 2025)

---

## ✓ Source and Sample of Data

### Data Source
- **Provider:** Yahoo Finance API
- **Access Method:** yfinance Python library
- **Data Type:** Historical daily OHLC (Open, High, Low, Close) + Volume
- **Data Quality:** Real-time market data from NSE

### Data Sample

**Period Covered:** November 8, 2023 to November 7, 2025 (2 years)  
**Total Trading Days:** 494 days

#### First 5 Trading Days:
| Date | Open (₹) | High (₹) | Low (₹) | Close (₹) | Volume |
|------|----------|----------|---------|-----------|---------|
| 2023-11-08 | 337.80 | 340.35 | 332.02 | 339.15 | 879,120 |
| 2023-11-09 | 339.85 | 345.38 | 338.15 | 341.09 | 750,240 |
| 2023-11-10 | 342.39 | 364.82 | 339.95 | 358.24 | 3,712,746 |
| 2023-11-13 | 358.64 | 371.94 | 350.86 | 367.51 | 3,020,750 |
| 2023-11-15 | 371.60 | 371.70 | 355.25 | 357.94 | 2,621,313 |

#### Last 5 Trading Days:
| Date | Open (₹) | High (₹) | Low (₹) | Close (₹) | Volume |
|------|----------|----------|---------|-----------|---------|
| 2025-11-03 | 1,024.00 | 1,040.50 | 1,018.30 | 1,030.70 | 1,501,905 |
| 2025-11-04 | 1,031.00 | 1,034.50 | 1,016.00 | 1,019.10 | 1,773,694 |
| 2025-11-05 | 1,019.10 | 1,019.10 | 1,019.10 | 1,019.10 | 0 |
| 2025-11-06 | 1,025.00 | 1,029.90 | 995.10 | 1,009.90 | 2,298,960 |
| 2025-11-07 | 1,007.00 | 1,022.50 | 1,000.80 | 1,020.00 | 1,719,482 |

**Performance:** Stock price increased from ₹339.15 to ₹1,020.00 (**+200.7% return** over 2 years)

---

## ✓ Estimated Parameters

### Input Parameters for Forward Pricing Model

| Parameter | Symbol | Value | Source/Justification |
|-----------|--------|-------|---------------------|
| **Spot Price** | S₀ | ₹1,020.00 | Current market price from Yahoo Finance (Nov 7, 2025) |
| **Risk-Free Rate** | r | 6.00% per annum | Indian Government Bond yield (10-year G-Sec benchmark) |
| **Dividend Yield** | q | 0.80% per annum | Conservative estimate based on FORTIS Healthcare's historical dividend policy and healthcare sector averages |
| **Time to Maturity** | T | Various (0.083 to 3 years) | Multiple maturities analyzed for comprehensive comparison |

### Calculation Formula

The forward price is calculated using the continuous compounding formula:

```
F = S₀ × e^((r - q) × T)
```

Where:
- **F** = Forward Price
- **S₀** = Current Spot Price (₹1,020.00)
- **r** = Risk-free rate (0.06 or 6%)
- **q** = Dividend yield (0.008 or 0.8%)
- **T** = Time to maturity (in years)
- **e** = Euler's number (2.71828...)

### Net Cost of Carry

**Net Carry Cost = r - q = 6.00% - 0.80% = 5.20% per annum**

This positive net carry cost indicates the market is in **contango** (forward prices trade at a premium to spot price).

---

## ✓ Forward Price Table

### Forward Prices for Different Maturities

| Maturity | Time (Years) | Spot Price (₹) | Forward Price (₹) | Difference (₹) | Difference (%) |
|----------|--------------|----------------|-------------------|----------------|----------------|
| **1 Month** | 0.083 | 1,020.00 | 1,024.43 | +4.43 | +0.43% |
| **3 Months** | 0.250 | 1,020.00 | 1,033.35 | +13.35 | +1.31% |
| **6 Months** | 0.500 | 1,020.00 | 1,046.87 | +26.87 | +2.63% |
| **9 Months** | 0.750 | 1,020.00 | 1,060.57 | +40.57 | +3.98% |
| **1 Year** | 1.000 | 1,020.00 | 1,074.44 | +54.44 | +5.34% |
| **1.5 Years** | 1.500 | 1,020.00 | 1,102.75 | +82.75 | +8.11% |
| **2 Years** | 2.000 | 1,020.00 | 1,131.79 | +111.79 | +10.96% |
| **3 Years** | 3.000 | 1,020.00 | 1,192.20 | +172.20 | +16.88% |

### Impact of Dividend Yield (1-Year Maturity Analysis)

| Dividend Yield Scenario | Dividend Yield (%) | Forward Price (₹) | Difference from Spot (₹) | Difference (%) |
|------------------------|-------------------|-------------------|-------------------------|----------------|
| **No Dividend** | 0.0% | 1,083.07 | +63.07 | +6.18% |
| **Low Dividend** | 0.5% | 1,077.67 | +57.67 | +5.65% |
| **Current Estimate** | 0.8% | 1,074.44 | +54.44 | +5.34% |
| **High Dividend** | 1.5% | 1,066.95 | +46.95 | +4.60% |
| **Very High Dividend** | 2.0% | 1,061.63 | +41.63 | +4.08% |

**Key Observation:** Each 1% increase in dividend yield reduces the 1-year forward price by approximately ₹10.50, demonstrating the inverse relationship between dividend yield and forward prices.

---

## ✓ Brief Discussion (1-2 Paragraphs)

### How Forward Price Changes with Maturity

The forward price exhibits a **positive exponential relationship** with time to maturity. As demonstrated in the forward price table, the premium over spot price increases from 0.43% for 1-month contracts to 16.88% for 3-year contracts. This exponential growth pattern occurs because the net cost of carry (r - q = 5.20%) compounds continuously over time. The 1-year forward price of ₹1,074.44 represents a 5.34% premium, while the 2-year forward nearly doubles this premium to 10.96%, and the 3-year forward reaches 16.88%. This non-linear relationship reflects the mathematical nature of continuous compounding in the formula F = S₀ × e^((r-q)×T), where the effect of time accelerates as the maturity period lengthens. Practically, this means that investors locking in longer-term forward contracts must pay increasingly higher premiums to compensate sellers for the extended opportunity cost of holding the underlying asset.

### Effect of Dividend Yield on Forward Prices

Dividend yield has a **significant negative impact** on forward prices, as demonstrated by comparing different dividend scenarios. When dividend yield increases from 0% to 2%, the 1-year forward price decreases from ₹1,083.07 to ₹1,061.63—a reduction of ₹21.44 (approximately 2% of spot price). This inverse relationship exists because dividends represent a financial benefit that accrues only to spot position holders, not to forward contract holders. In our FORTIS analysis with an estimated 0.8% dividend yield, the forward prices are reduced by approximately ₹8.63 for 1-year maturity compared to a no-dividend scenario. The formula F = S₀ × e^((r-q)×T) explicitly shows dividends (q) acting as a reduction factor that partially offsets the risk-free rate (r). This mechanism ensures that forward contracts are fairly priced—if dividends were ignored, forward buyers would be unfairly advantaged, as they would pay the same forward price despite missing out on dividend income during the contract period. For FORTIS Healthcare, which maintains a modest dividend policy typical of growth-oriented healthcare companies, this effect moderately reduces forward premiums compared to non-dividend-paying stocks.

---

## Additional Insights

### Market Implications

1. **Contango Market:** FORTIS forward prices are in contango (F > S₀), indicating positive net carrying costs. This is typical for financial assets where the risk-free rate exceeds dividend yield.

2. **Arbitrage-Free Pricing:** The forward prices calculated represent theoretical fair values. Any significant deviation in actual market forward prices would create arbitrage opportunities.

3. **Hedging Applications:** 
   - Investors can lock in the 1-year forward price of ₹1,074.44 today
   - If expecting FORTIS to trade above this level, long forward position is profitable
   - If expecting prices below ₹1,074.44, short forward position is advantageous

4. **Risk Management:** Forward contracts eliminate spot price uncertainty but introduce basis risk and counterparty risk.

### Limitations and Assumptions

- Assumes constant risk-free rate and dividend yield over the contract period
- Ignores transaction costs and bid-ask spreads
- Based on continuous compounding (theoretical model)
- Dividend yield estimated from sector averages (actual dividends may vary)

---

## Conclusion

This forward pricing analysis demonstrates that FORTIS Healthcare forward prices increase exponentially with maturity due to positive net carrying costs (5.20% per annum), while dividend yield acts as a moderating factor that reduces forward premiums. The 1-year forward price of ₹1,074.44 represents a 5.34% premium over the current spot price of ₹1,020.00, providing a fair theoretical value for forward contracts on FORTIS stock. These calculations are based on real market data and realistic parameter estimates for the Indian equity market.

---

**Report Generated:** November 7, 2025  
**Analysis Tool:** Python (Jupyter Notebook)  
**Data Verification:** All prices and calculations verified against Yahoo Finance real-time data
