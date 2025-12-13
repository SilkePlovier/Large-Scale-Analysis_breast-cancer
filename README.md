# Large-Scale Analysis of Breast Cancer

## Introduction
This repository contains code, data, and documentation for a large-scale survival analysis of breast cancer patients. The project investigates a univariate hypothesis and multivariate hypothesis, supported by Spearmann's rank correlation, cox model, survival curves and machine learning.

## Objectives
- Identify survival differences based on ESR1 expression and treatment status.
- Understand relationship between ADHD11 and tumor size.
- Machine-learning analyses to confirm the predictive utility of transcriptomic data.
- Apply robust preprocessing, imputation, and outlier detection to ensure statistical integrity.
- Generate reproducible survival plots and model outputs for publication.

## Repository Structure
- Raw R scripts
- Breast-cancer-dataset_Official-R-script.html: official html file with all results and figures
- Project (1).ipynb: file for Machine Learning
- README.md

## Key Variables
- `ESR1`: Expression level (continuous or stratified)
- `chemo treated:ch1`: Binary chemotherapy status
- `endocrine treated:ch1`: Binary endocrine therapy status
- `overall survival days:ch1`, `overall survival event:ch1`: Survival time and censoring
- `age at diagnosis:ch1`, `tumor size:ch1`, receptor status variables

## Example Outputs
- Spearmann's rank correlation
- Cox model summary with hazard ratios and p-values
- Survival curves with risk tables
- Stratified survival estimates based on model-informed groups
- Machine learning? what is the output?
