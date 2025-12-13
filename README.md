# Large-Scale Analysis of Breast Cancer

## Introduction
This repository contains code, data, and documentation for a large-scale survival analysis of breast cancer patients. The project investigates the prognostic and predictive value of ESR1 expression, chemotherapy, and endocrine therapy using Cox proportional hazards models and Kaplan–Meier survival curves.

## Objectives
- Identify survival differences based on ESR1 expression and treatment status.
- Quantify interaction effects between ESR1 and chemotherapy.
- Apply robust preprocessing, imputation, and outlier detection to ensure statistical integrity.
- Generate reproducible survival plots and model outputs for publication.

## Repository Structure




## Methods Summary
- **Imputation**: Missing data handled via KNN (`VIM::kNN`) with Ki67 included during imputation.
- **Outlier Detection**: Multivariate outliers removed using Mahalanobis distance (excluding ESR1 to preserve biological signal).
- **Modeling**: Cox regression adjusted for age, tumor size, receptor status, and treatment variables.
- **Visualization**: Kaplan–Meier curves stratified by ESR1 × Chemo, derived from Cox model strata.

## Key Variables
- `ESR1`: Expression level (continuous or stratified)
- `chemo treated:ch1`: Binary chemotherapy status
- `endocrine treated:ch1`: Binary endocrine therapy status
- `overall survival days:ch1`, `overall survival event:ch1`: Survival time and censoring
- `age at diagnosis:ch1`, `tumor size:ch1`, receptor status variables

## Example Outputs
- Cox model summary with hazard ratios and p-values
- Survival curves with risk tables
- Stratified survival estimates based on model-informed groups

## Getting Started
### Prerequisites
- R ≥ 4.2
- Required packages: `survival`, `survminer`, `VIM`, `dplyr`, `ggplot2`, `gridExtra`

### Installation
```r
install.packages(c("survival", "survminer", "VIM", "dplyr", "ggplot2", "gridExtra"))
