***🧠 FX Forecast & Long/Short Trading Strategy (Spring 2025 Final)***

**This repository contains a two-part final project for the Spring 2025 course on real-time FX analytics and algorithmic trading. The project leverages Polygon real-time financial data, PyCaret machine learning models, and a custom long/short trading strategy to forecast currency pair behaviors and simulate basic algorithmic trading decisions.**

***📁 Project Structure***

Final.ipynb: Full pipeline for data preprocessing, feature engineering, and regression-based analysis.

Final_Pycaret.ipynb: Classification modeling using PyCaret to label currency pairs as FORECASTABLE, NON-FORECASTABLE, or UNDEFINED.

Final_strategy.ipynb: Implements a dynamic long/short strategy using slope-based trend analysis on USDGBP and USDJPY


***🔍 Part 1: Feature Forecasting & Classification***

Goal: Predict the behavior of a synthetic base currency pair using regression and classify all CPs into forecastability categories.

Data Source: Real-time data from Polygon.io

Currency Pairs: USDEUR, EURCHF, GBPEUR, USDGBP, GBPCHF, USDCHF, USDCAD, USDJPY, USDINR, USDCNY, USDAUD

Regression Features:

· Mean price, normalized volatility (VOL), fractal dimension (FD)

· Correlation with EURUSD and BTC (as macroeconomic proxies)

Classification Targets:

· FORECASTABLE (F)

· NON-FORECASTABLE (N)

· UNDEFINED (U)

📌 Tools: PyCaret, scikit-learn, pandas, numpy

***📈 Part 2: Long/Short Trading Strategy***

Goal: Execute a 3-step long/short strategy based on slope direction from 20-point univariable regressions.

Currency Pairs Used: USDGBP and USDJPY

Method:

· Calculate trend slopes from historical price data.

· Determine position size proportionally based on slope strength.

· Perform L/S trades at hours #5, #6, and #7; exit at hour #8.

· Use adjusted ratio between USDJPY and USDGBP to normalize trade volumes.

Accounting:

· $100 simulated per L/S step.

· Profit/loss computed and aggregated.

***📊 Results Summary***

Successful classification of base and non-base CPs using PyCaret.

Long/Short strategy produced interpretable P/L over 3 steps.

Demonstrates how regression + classification models can support basic algorithmic decisions in FX markets.
