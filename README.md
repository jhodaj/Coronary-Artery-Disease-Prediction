# Coronary Artery Disease Prediction Using Frequentist and Bayesian Logistic Regression

## Overview

This project analyzes patient-level cardiovascular data to identify factors associated with coronary artery disease (CAD) and predict disease status using both frequentist and Bayesian logistic regression.

The analysis compares classical logistic regression with Bayesian models under alternative prior specifications and uses posterior simulation and Bayes factors to assess predictor importance.

## Data

The analysis uses the UCI Heart Disease dataset accessed through Kaggle.

- 920 patient records
- 6 predictors used in modeling:
  - Age
  - Sex
  - Chest pain type
  - Resting blood pressure
  - Serum cholesterol
  - Maximum heart rate achieved
- Binary outcome: CAD present vs. absent
- 80/20 train-test split:
  - 736 training observations
  - 184 test observations

Missing values in continuous predictors were imputed using means calculated within age and sex groups, and categorical variables were recoded for modeling.

## Methods

- Exploratory data analysis and visualization
- Missing-data handling and categorical-variable encoding
- Multicollinearity assessment
- Frequentist logistic regression
- Bayesian logistic regression with informative and non-informative priors
- Bayes-factor comparison for predictor importance
- Markov Chain Monte Carlo (MCMC) posterior sampling
- Held-out test-set prediction

## Results

The frequentist and Bayesian analyses produced consistent conclusions.

Age, sex, chest pain type, and maximum heart rate were identified as important predictors of CAD, while resting blood pressure and cholesterol showed weaker evidence in the fitted models.

The logistic-regression model achieved **78.8% classification accuracy on the held-out test set**.

## Tools

R | dplyr | ggplot2 | MCMCpack | LearnBayes | caret | coda

## Repository Contents

- `README.md` — project overview and results
- `CAD_Logistic_Regression_Analysis.Rmd` — complete analysis and modeling workflow
- `BDA-Final-Project1.pdf` — full project report
- `heart_disease_uci.csv` — dataset, if redistribution is permitted

