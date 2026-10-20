# PSX Smart Portfolio and Investment Advisor Agent

An interactive, Python-based investment research and portfolio planning application for the **Pakistan Stock Exchange (PSX)**. Built with Streamlit, this project helps users explore stock performance, analyze market momentum, estimate portfolio allocations, and forecast long-term wealth accumulation through a customizable monthly investment plan.

The application combines historical stock market data, technical indicators, dividend yield estimates, and compound growth calculations to support investment research and financial planning.

##  Project Overview

The PSX Smart Portfolio & Investment Advisor Agent is designed to make stock market research more accessible to beginners, students, and individual investors interested in the Pakistan Stock Exchange.

Users can select companies from different sectors, define their investment budget, choose an investment horizon, and generate portfolio analysis and projections through an interactive dashboard.

**Project Type:** Financial Data Analysis & Investment Research  
**Market:** Pakistan Stock Exchange (PSX)  
**Interface:** Streamlit Web Application  
**Language:** Python

## Key Features

- **Multi-Sector Stock Selection:** Explore companies across technology, banking, fertilizer, oil and gas, cement, power generation, refinery and chemicals, and pharmaceuticals.
- **Historical Stock Price Analysis:** Retrieve historical stock market data using Yahoo Finance.
- **Performance Tracking:** Calculate approximate 1-month, 6-month, and 1-year stock returns.
- **RSI Technical Indicator:** Calculate the Relative Strength Index (RSI) to help examine market momentum.
- **Dividend Yield Estimates:** Include predefined dividend yield estimates for selected companies in portfolio analysis.
- **Custom Portfolio Allocation:** Estimate how many whole shares can be purchased for each selected company using an equal budget allocation.
- **Long-Term Investment Forecasting:** Project potential portfolio value using configurable annual growth assumptions.
- **Monthly SIP Planning:** Estimate investment outcomes based on a recurring monthly contribution over a selected period.
- **Interactive Dashboard:** Configure investment settings and view results in a user-friendly Streamlit interface.

##  Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | Interactive web application and dashboard |
| yfinance | Historical stock market data retrieval |
| Pandas | Data manipulation and tabular analysis |
| NumPy | Numerical computations |
| TA (Technical Analysis Library) | RSI technical indicator |
| datetime | Date and time utilities |

##  Supported Sectors

The application includes a predefined selection of companies from the following sectors:

- Technology & Telecom
- Commercial Banks
- Fertilizer
- Oil & Gas Exploration
- Cement
- Power Generation
- Refinery & Chemicals
- Pharmaceuticals

Users can select individual companies from the sidebar to customize their analysis.

##  Investment Analysis Modes

### 1. Short-Term Momentum Analysis

Designed for users exploring short-term market performance.

Features include:
- Recent stock price and historical return analysis.
- RSI-based momentum monitoring.
- Equal allocation of the selected investment budget across eligible companies.
- Estimated whole-share quantities and investment amounts.

### 2. Long-Term Wealth Accumulation

Designed for users exploring the potential impact of regular investing over time.

Features include:
- Monthly investment budget configuration.
- Investment duration selection from 1 to 10 years.
- Configurable annual growth assumptions.
- Estimated total capital invested.
- Projected portfolio value and potential profit.
- Estimated dividend income based on predefined dividend yield assumptions.

Available growth assumptions include conservative, moderate, aggressive, and a fixed fallback assumption when the historical CAGR option is selected.

##  Installation & Setup

Follow these steps to run the project locally.

### Prerequisites

- Python 3.9 or later
- pip package manager
- Internet connection for retrieving stock market data

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

Navigate to the project directory:

```bash
cd YOUR-REPOSITORY
```

### Step 2: Create a Virtual Environment (Recommended)

```bash
python -m venv venv
```

Activate the environment.

**Windows:**

```bash
venv\Scripts\activate
```

**Linux / macOS:**

```bash
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install streamlit yfinance pandas numpy ta
```

### Step 4: Run the Application

If your Python file is named `app.py`, execute:

```bash
streamlit run app.py
```

Streamlit will launch the application in your default browser or provide a local URL to open it.

##  How to Use

1. Launch the application.
2. Select your investment goal from the sidebar.
3. Enter your total investment budget or monthly contribution.
4. Choose the investment duration.
5. Select an annual market growth assumption.
6. Expand the sector lists and select your preferred companies.
7. Click **Generate Portfolio Prediction**.
8. Review the stock performance metrics, estimated share allocation, and long-term investment projections.

##  Core Calculations

### Historical Stock Returns

The application estimates historical returns using closing prices:

\[
\text{Return (\%)} =
\left(\frac{\text{Latest Price}}{\text{Previous Price}}-1\right)\times100
\]

### Relative Strength Index (RSI)

The application calculates a 14-period RSI using the `ta` technical analysis library.

RSI is a momentum indicator commonly interpreted using the following reference levels:

- RSI above 70: Potentially overbought conditions.
- RSI below 30: Potentially oversold conditions.

These levels are indicators, not guaranteed buy or sell signals.

### Monthly Investment Projection

The application estimates the future value of recurring monthly contributions using a compound growth formula, with an additional adjustment for contributions made at the beginning of each period.

The general calculation is:

\[
FV=P\left(\frac{(1+r)^n-1}{r}\right)(1+r)
\]

Where:

- \(FV\) = Projected future value
- \(P\) = Monthly investment amount
- \(r\) = Assumed monthly growth rate
- \(n\) = Total number of monthly contributions

The model also estimates dividends separately using predefined yield assumptions.

**Important:** These calculations are simplified estimates. The current implementation does not model actual dividend payment dates, dividend reinvestment, taxes, brokerage charges, inflation, or changes in contribution amounts.

##  Data Sources & Limitations

- Historical stock prices are retrieved through Yahoo Finance using `yfinance`.
- Data availability depends on the provider and the ticker symbols configured in the application.
- Dividend yields are predefined estimates in the code; they are not automatically retrieved from current company financial statements.
- The historical CAGR option currently uses a fixed 10% annual growth assumption rather than calculating CAGR from historical data.
- The long-term projection is a mathematical scenario, not a trained AI or machine learning prediction model.
- Portfolio allocation uses equal weighting and whole-share quantities; it does not optimize allocations using risk, volatility, or transaction costs.
- Market data may be delayed, incomplete, or unavailable for some symbols.

Actual PSX ticker compatibility and data accuracy should be verified before relying on the results.

##  Future Improvements

Potential enhancements for future versions include:

- Integration of verified PSX market data and company financial statements.
- Automated dividend history and dividend yield calculations.
- Fundamental analysis using P/E, P/B, ROE, debt ratios, and earnings growth.
- Historical CAGR calculation based on actual market data.
- Portfolio diversification and risk analysis.
- Dividend reinvestment and inflation-adjusted projections.
- Interactive charts for stock prices, returns, and portfolio growth.
- Machine learning models for research-oriented forecasting.
- Backtesting and performance evaluation.
- Deployment as a publicly accessible web application.

##  Project Objective

The objective of this project is to apply Python programming, financial data analysis, and interactive dashboard development to a practical investment research problem. It aims to help users understand stock performance, explore portfolio allocation, and evaluate different long-term investment scenarios.

##  Disclaimer

This application is intended for **educational and research purposes only**. It does not provide guaranteed returns or personalized financial advice. Stock market investments involve risk, and historical performance does not guarantee future results.

Always verify market prices, company financial information, and dividend announcements from reliable sources before making investment decisions.

##  Author

**Zeeshan Ahmad**

GitHub: Zeeshan-406 (https://github.com/YOUR-GITHUB-Zeeshan-406)

---

*If you find this project useful, consider giving the repository a star .*
