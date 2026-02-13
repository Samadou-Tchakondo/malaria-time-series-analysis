# Time Series Analysis of Confirmed Malaria Cases Using ARIMA, SARIMA and ARIMAX Models

## Overview

This project applies advanced time series modelling techniques to monthly malaria surveillance data collected in Togo between 2022 and 2024.

The objective is to characterise temporal dynamics, detect seasonality, and generate forecasts to support evidence-based public health planning.

The analysis follows the **Box–Jenkins framework** and compares:

* **ARIMA** (non-seasonal model)
* **SARIMA** (seasonal model)
* **ARIMAX** (model including climatic covariates)

---

## Objectives

* Examine temporal structure (trend, seasonality, autocorrelation)
* Test stationarity using Augmented Dickey–Fuller procedures
* Identify appropriate ARIMA-family models
* Compare competing models using AIC/BIC criteria
* Produce forecasts for 2025–2026 malaria burden
* Demonstrate reproducible epidemiological modelling in R

---

## Project Structure

```
Time-Series-Analysis-Malaria/
│
├── data/                              # Raw surveillance dataset (.sav)
├── Time Series Analysis.Rmd           # Main reproducible analysis
├── Time-Series-Analysis.html          # Rendered report
├── Time-Series-Analysis-Malaria.Rproj # R project file
└── README.md                          # Project documentation
```

---

## Methods

The analysis uses:

* Time series decomposition (additive vs multiplicative)
* Stationarity diagnostics (ADF test)
* ACF/PACF for model identification
* SARIMA modelling for seasonal epidemiological data
* Forecast validation using out-of-sample testing

---

## Key Findings

* Strong and stable annual malaria seasonality detected.
* **SARIMA(0,0,1)(1,1,0)[12]** provided the best model fit.
* Climatic covariates did not significantly improve predictive performance.
* Forecasts indicate persistence of seasonal peaks through 2026.

---

## Reproducibility

All analyses were conducted in **R** using the following packages:

```
forecast
tseries
tidyverse
haven
```

To reproduce the analysis:

```r
rmarkdown::render("Time Series Analysis.Rmd")
```

---

## Citation

If you use this work, please cite:

**TCHAKONDO, S. (2026).**
*Time Series Analysis of Confirmed Malaria Cases Using ARIMA, SARIMA and ARIMAX Models.*
SRM Institute of Science and Technology.
Available at:
https://github.com/Samadou-Tchakondo/malaria-time-series-analysis

---

## Author

**Samadou TCHAKONDO**
Biostatistician & Epidemiologist
SRM Institute of Science and Technology, India
ORCID: https://orcid.org/0009-0006-6747-3170

---

## License

This project is released under the MIT License.
