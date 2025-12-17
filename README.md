# Measuring Joy Before the Storm  
## A Regression Analysis of Pre-COVID Happiness (2019)

## Overview
This repository contains a **multiple linear regression analysis** of national happiness levels using data from the **2019 World Happiness Report**, the last year before the COVID-19 pandemic.

The project aims to identify and quantify the key socio-economic and perception-based factors associated with subjective well-being across countries, using a rigorous statistical modeling and diagnostic workflow.

The full analysis is implemented using **Sweave (`.Rnw`)**, ensuring a fully reproducible integration of R code, statistical output, and LaTeX-based reporting.

---

## Research Question
**Can the happiness score of a country in 2019 be explained using measurable national indicators, and which of these indicators are the most influential?**

---

## Dataset
- **Source:** World Happiness Report 2019 (UN Sustainable Development Solutions Network)
- **Observations:** 156 countries
- **Response variable:**  
  - `Score` — average life evaluation score (Cantril ladder)
- **Predictors:**
  - GDP per capita
  - Social support
  - Healthy life expectancy
  - Freedom to make life choices
  - Generosity
  - Perceptions of corruption

The dataset contains no missing values and all predictors are numeric, making it well-suited for regression analysis.

---

## Methodology
### 1. Exploratory Data Analysis
- Pairwise scatterplots and visual inspection
- Assessment of linear relationships and collinearity
- Preliminary insights into predictor relevance

### 2. Regression Modeling
- Simple linear regression for each predictor
- Full multiple linear regression model
- Model comparison using R² and adjusted R²
- Stepwise variable selection based on AIC

### 3. Regression Diagnostics
- Homoscedasticity and residual independence checks
- Normality assessment (Q-Q plots and Kolmogorov–Smirnov test)
- Linearity validation using component-plus-residual plots
- Detection of outliers and influential observations

### 4. Model Refinement
- Iterative removal of influential observations
- Stability analysis of coefficients and goodness-of-fit
- Final refined model with improved explanatory power

---

## Key Results
- **GDP per capita, social support, and healthy life expectancy** are the strongest predictors of national happiness.
- **Generosity** shows limited explanatory power and is consistently non-significant.
- The refined model explains over **83% of the variability** in happiness scores (Adjusted R² ≈ 0.835).
- Regression assumptions are largely satisfied, with only mild autocorrelation detected.

---

## Reproducible Workflow
The analysis is written in a **Sweave (`.Rnw`) file**, which:
- Integrates R code directly into a LaTeX document
- Produces a publication-quality PDF
- Ensures full reproducibility of all results

---

## Repository Structure
├── Group_coursework_def.Rnw      # Main Sweave analysis
├── Group_coursework_def.pdf      # Compiled report
├── 2019.csv                      # Dataset
└── README.md
