
# Volatility Term Structure

This repository contains Python code to analyze **volatility skew** and **term structure**, which are essential concepts in options trading. The aim is to help traders, researchers, and financial professionals gain insights into the market's volatility dynamics.

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Example Analysis](#example-analysis)
- [License](#license)

## Introduction

- **Volatility Skew**: This refers to the variation in implied volatility of options across different strike prices. A steeper skew may indicate market participants' perception of potential downside risks.
  
- **Volatility Term Structure**: This is the curve that plots implied volatility against time to expiration. A steepening curve may suggest increasing uncertainty or risk perception for longer time horizons.

## Installation

### Prerequisites
- Python 3.x
- [pandas](https://pandas.pydata.org/)
- [numpy](https://numpy.org/)
- [matplotlib](https://matplotlib.org/)
- [scipy](https://scipy.org/)
- [yfinance](https://pypi.org/project/yfinance/)

### Installation Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/kushalgowdagv/volatility_term_structure.git
   ```

2. Navigate to the project directory:

   ```bash
   cd volatility_term_structure
   ```

3. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

This script uses Python libraries such as `numpy`, `pandas`, and `yfinance` to fetch and manipulate options data from Yahoo Finance. Here's how you can use it:

1. **Import Libraries**:
   Ensure the following libraries are imported:
   ```python
   import numpy as np
   import pandas as pd
   import yfinance as yf
   import datetime
   import matplotlib.pyplot as plt
   ```

2. **Fetch Options Data**:
   Use the `fetch_option_data` function to fetch option chain data for a given stock index:
   ```python
   def fetch_option_data(ticker):
       # Implementation details
   ```

   - The function creates a `Ticker` object using `yf.Ticker(ticker)` and retrieves options data.
   - It returns a `DataFrame` with details like option type, days to expiration, and implied volatility.

3. **Analyze the Data**:
   - Print available expiration dates.
   - Select specific expiration dates and call options.
   - Plot implied volatility skew and term structure based on your analysis.

## Example Analysis

Here's a brief walkthrough of an example analysis:

1. **Fetch Options Data for NASDAQ**:
   ```python
   option_data = fetch_option_data("^NDX")
   ```

2. **Filter and Analyze Data**:
   - Select call options and filter based on expiration dates.
   - Filter out low implied volatility values (`implied volatility >= 0.005`).

3. **Plot Implied Volatility Skew**:
   ```python
   # Set the strike price as the index
   # Plot the skew for a selected expiration date
   ```

4. **Plot Implied Volatility Term Structure**:
   ```python
   # Set the expiration date as the index
   # Plot the term structure for a specific strike price
   ```

The code produces plots for both the **Implied Volatility Skew** (variation across strike prices) and **Implied Volatility Term Structure** (variation across expiration dates).

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

