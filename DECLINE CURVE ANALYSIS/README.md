# Production Forecasting and Reserve Estimation Using Decline Curve Analysis (DCA)

## Overview

This project implements Decline Curve Analysis (DCA) using Python to forecast production performance and estimate reserves from historical well data. Both exponential and hyperbolic decline models are applied, and results are compared using error analysis to identify the most suitable model.

---

## Objectives

* Estimate decline parameters (qi, D, Di, b) from production data
* Forecast future production rates
* Calculate cumulative production (Np)
* Estimate Ultimate Recovery (EUR)
* Compare model performance using error analysis (SSE)

---

## Methodology

### Data Preparation

Historical production rate versus time data is used as input.

### Exponential Decline Model

* Linearization using ln(q) versus time
* Parameters estimated using linear regression
* Assumes constant decline rate

### Hyperbolic Decline Model

* Nonlinear curve fitting using SciPy
* Estimates qi, Di, and b
* Captures variable decline behavior

### Model Comparison

* Compared using Sum of Squared Errors (SSE)
* Lower SSE indicates better model fit

### Cumulative Production (Np)

* Analytical solutions used for both models
* Special handling for b ≈ 1 (harmonic case) to avoid instability

### EUR Estimation

* Calculated at economic limit rate (q_econ)

---

## Key Results

* Hyperbolic model provided significantly lower error compared to exponential
* Estimated b ≈ 1, indicating near-harmonic decline behavior
* Hyperbolic model better represents reservoir performance
* Indicates longer production life and higher EUR

---

## Engineering Insights

* Exponential decline is useful for late-time approximation
* Hyperbolic decline captures real reservoir behavior more accurately
* Model selection should be data-driven, not assumed
* Special care is required when b approaches 1, where harmonic equations must be used

---

## Tech Stack

* Python
* NumPy
* Matplotlib
* SciPy

---

## Output Visualizations

* Production decline curves (actual vs forecast)
* Semi-log plot for linear regression
* Model comparison plots
* Cumulative production curves

---

## Key Learning Outcomes

* Applied Decline Curve Analysis (Arps model) on production data
* Performed regression and nonlinear curve fitting
* Interpreted reservoir behavior using decline parameters
* Compared engineering models using statistical error metrics

---

## Conclusion

The hyperbolic decline model was found to be more suitable for the dataset due to its ability to capture variable decline behavior. The project demonstrates a complete workflow of production forecasting and reserve estimation used in practical reservoir engineering applications.

---

## How to Run

1. Clone the repository
2. Open the .ipynb file in Jupyter Notebook or Google Colab
3. Run all cells

---

### Author

**Mani Kanta**  
Petroleum Engineering  
IIT (ISM) Dhanbad

---
