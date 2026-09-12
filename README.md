# Medical Cost Prediction — Statistical Analysis

## Overview

This project presents a statistical analysis of annual healthcare expenditure using the **Medical Cost Prediction Dataset**. The dataset contains **5,000 patient records and 20 demographic, clinical, lifestyle, and financial variables**, with `annual_medical_cost` as the target variable.

The analysis was completed as a semester project for **Advanced Statistics (STAT222)** and focuses on identifying the major factors associated with healthcare costs.

## Objectives

The project aims to:

- Analyze the distribution of annual medical costs.
- Identify the best-fitting probability distribution for medical costs.
- Determine whether medical costs differ across insurance types and physical activity levels.
- Identify significant predictors of medical cost using multiple linear regression.
- Validate the findings using nonparametric statistical tests.
- Generate visualizations to understand relationships, trends, and group differences.

## Dataset

The dataset contains 5,000 patient records and includes variables such as:

- Age
- BMI
- Gender
- Smoking status
- Diabetes
- Hypertension
- Heart disease
- Insurance type
- City type
- Physical activity level
- Stress level
- Daily steps
- Sleep hours
- Doctor visits per year
- Hospital admissions
- Medication count
- Insurance coverage percentage
- Previous-year medical cost
- Annual medical cost

The target variable is:

`annual_medical_cost` — annual healthcare expenditure in US dollars.

The report states that the dataset contains no missing values or duplicate records.

## Statistical Methods

### 1. Exploratory Data Analysis

The project uses:

- Descriptive statistics
- Histograms
- Box plots
- Pearson correlation heatmaps
- Scatter matrix analysis

These were used to understand distributions, identify patterns, and examine relationships between variables.

### 2. ANOVA

Both **One-Way ANOVA** and **Two-Way ANOVA** were applied.

The analysis examined:

- Differences in medical cost across insurance types.
- The effect of physical activity level.
- The interaction between insurance type and physical activity level.

### 3. Probability Distribution Fitting

Four probability distributions were fitted to annual medical cost:

- Normal
- Log-Normal
- Gamma
- Exponential

Model fit was evaluated using:

- Kolmogorov-Smirnov (KS) test
- Anderson-Darling test
- AIC
- BIC

The **Log-Normal distribution** produced the lowest AIC and was identified as the best-fitting distribution in the report.

### 4. Multiple Linear Regression

A multiple linear regression model was developed using **17 predictors** and a log-transformed medical cost target.

Predictors included demographic, clinical, lifestyle, healthcare utilization, insurance, and previous-cost variables.

The model achieved an **Adjusted R² of approximately 0.892** according to the report.

Regression assumptions were assessed using:

- Shapiro-Wilk test
- Breusch-Pagan test
- Durbin-Watson statistic
- Variance Inflation Factor (VIF)

### 5. Nonparametric Statistics

The project also applied distribution-free statistical tests:

- Mann-Whitney U test
- Kruskal-Wallis H test
- Spearman rank correlation
- Chi-Square test of independence

These tests were used to validate group differences and identify monotonic relationships without relying solely on parametric assumptions.

## Key Findings

The analysis reported several important findings:

- Insurance type was associated with substantial differences in annual medical costs.
- The **Log-Normal distribution** provided the best fit among the tested distributions based on AIC.
- **Hospital admissions, medication count, smoking status, and previous-year cost** were identified as important predictors in the regression analysis.
- Smokers were reported to have higher medical costs than non-smokers.
- Hospital admissions showed one of the strongest positive monotonic relationships with annual medical cost.
- Higher physical activity levels were associated with lower medical costs in the reported group comparisons.
- The regression model explained a large proportion of variation in the log-transformed medical cost.

## Analytical Workflow

The project followed these main stages:

1. **Data ingestion and cleaning**
2. **Data quality checks**
3. **Feature encoding and transformation**
4. **Exploratory data analysis**
5. **Inferential statistical testing**
6. **Regression modeling and diagnostics**
7. **Probability distribution fitting**
8. **Nonparametric validation**
9. **Visualization and interpretation**
10. **Final reporting**

## Technologies and Libraries

The project was developed using Python and statistical/data-analysis libraries including:

- Python 3.x
- Pandas
- NumPy
- SciPy
- Statsmodels
- Matplotlib
- Seaborn

## Project Structure

A suggested repository structure is:

```text
Medical-Cost-Prediction/
│
├── README.md
├── data/
│   └── medical_cost_dataset.csv
│
├── notebooks/
│   └── medical_cost_analysis.ipynb
│
├── src/
│   └── analysis.py
│
├── figures/
│   ├── histograms/
│   ├── boxplots/
│   ├── correlations/
│   └── regression_diagnostics/
│
└── report/
    └── Medical_Cost_Analysis_Report.pdf
```

The exact file structure may differ depending on the contents of the GitHub repository.

## Limitations

The report identifies several limitations:

- The dataset is cross-sectional, so causal relationships cannot be established.
- Some lifestyle variables may contain measurement error.
- Heteroscedasticity remained in the regression diagnostics.
- The dataset does not contain a time-series component.
- Some healthcare utilization variables may conceptually overlap.

## Future Work

Possible extensions include:

- Applying a Gamma Generalized Linear Model (GLM) with a log link.
- Performing stratified regression for different age or disease-risk groups.
- Using clustering to identify patient profiles.
- Incorporating longitudinal healthcare data.
- Applying Bayesian regression for probabilistic cost forecasting.

## Academic Context

**Course:** Advanced Statistics (STAT222)  
**Program:** BS Data Science  
**Semester:** Spring 2026  
**Project:** Medical Cost Prediction — Statistical Analysis

## Authors

- Fatima Ahmed
- Maryam Asif

## Note

This repository is intended for **academic and educational purposes**. Statistical results and interpretations are based on the dataset and analysis presented in the accompanying project report.
