# Analysing Stock Market Returns Against Market Volatility

A time series analysis and forecasting study exploring the relationship between NASDAQ returns and VIX volatility using Meta's Prophet forecasting framework.

**Live report:** [View full analysis](https://0aarontahiri.github.io/Analysing-Market-Returns-Against-Market-Volatility/)

---

## Overview

This project investigates the behavioural relationship between two closely linked financial time series - the NASDAQ Composite Index and the CBOE Volatility Index (VIX) - using daily data from 2000 to 2025. The period captures multiple distinct market regimes including the dot-com crash, the 2008 financial crisis, and the COVID-19 pandemic.

The analysis applies Meta's Prophet forecasting system to model long-term trends in both series and examines the inverse relationship between equity market returns and implied volatility.

---

## Key Findings

**Inverse relationship confirmed** - periods of declining NASDAQ performance consistently coincide with spikes in VIX, reflecting the well-documented flight-to-safety dynamic in equity markets.

**NASDAQ is forecastable long-term** - Prophet captures the long-term bullish trend in NASDAQ effectively, though short-term fluctuations remain difficult to predict due to the stochastic nature of financial markets.

**VIX is harder to forecast** - the mean-reverting, spike-driven nature of VIX makes it substantially more difficult to model than equity price trends. Prophet captures baseline behaviour but misses the sharp stress spikes that define VIX dynamics.

**Negative returns cluster with high volatility** - log return analysis confirms that the largest negative daily returns in NASDAQ consistently occur during elevated VIX regimes, suggesting volatility as a useful risk signal for equity positioning.

---

## Methodology

- Data sourced from Yahoo Finance via the `quantmod` R package
- Daily NASDAQ Composite and VIX data from 2000 to present
- Exploratory time series analysis including trend decomposition and visual inspection
- Prophet model fitted separately to NASDAQ and VIX with uncertainty intervals
- Log return calculation and scatter analysis against contemporaneous VIX levels

---

## Structure

| File | Description |
|---|---|
| `Analysing-Market-Returns-Against-Market-Volatility.Rmd` | Full R Markdown source code |
| `index.html` | Knitted HTML report (rendered via GitHub Pages) |

---

## Tools and Libraries

R, RMarkdown, Prophet, quantmod, ggplot2, dplyr

---

## Author

Aaron Tahiri - BSc Mathematics, Queen Mary University of London, 2025
