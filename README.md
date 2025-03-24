# Advanced Customer Analytics Using MLE

## Project Overview
This repository contains a comprehensive analysis of customer behavior using advanced statistical modeling techniques. The project implements Maximum Likelihood Estimation (MLE) to develop Poisson and Negative Binomial Distribution (NBD) models for predicting customer exposure and purchase patterns.

## Table of Contents
- [Introduction](#introduction)
- [Project Objectives](#project-objectives)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Technical Implementation](#technical-implementation)
- [Usage](#usage)
- [Skills Demonstrated](#skills-demonstrated)

## Introduction
This project applies sophisticated statistical models to analyze and predict customer behavior in two key scenarios:
1. **Billboard Exposure Analysis**: Modeling how many times individuals are exposed to advertising billboards
2. **Online Retail Behavior Analysis**: Predicting customer visits to Barnes & Noble's website compared to Amazon

The analysis leverages the strengths of both Poisson and NBD models, including their regression variants, to account for customer heterogeneity and provide more nuanced predictions.

## Project Objectives
- Implement and compare Poisson and NBD models for count data prediction
- Develop regression variants that incorporate customer characteristics
- Evaluate model performance using AIC, BIC, and likelihood ratio tests
- Extract actionable business insights from statistical analyses
- Predict future customer behaviors based on historical patterns

## Methodology

### Data Processing
- Transformed raw data into appropriate formats for different modeling approaches
- Handled missing values and outliers through systematic cleaning procedures
- Created specialized datasets (books01.csv and books02.csv) for different analytical approaches

### Modeling Approach
The project implemented four distinct modeling approaches:

1. **Poisson Model**: Assumes equal exposure probability for all customers
   - Applied to both billboard exposure and website visit data
   - Optimized via MLE to find the ideal λ parameter

2. **NBD Model**: Accounts for heterogeneity in customer behavior
   - Incorporates parameters for both purchasing (n) and churning (α)
   - Better captures the overdispersion in customer data

3. **Poisson Regression**: Incorporates customer-specific variables
   - Includes demographic factors like age, income, and household size
   - Allows for personalized prediction based on customer profile

4. **NBD Regression**: Combines the advantages of NBD with regression
   - Accounts for both heterogeneity and customer characteristics
   - Provides the most comprehensive modeling approach

### Model Evaluation
Models were rigorously evaluated using:
- Log-likelihood values
- Akaike Information Criterion (AIC)
- Bayesian Information Criterion (BIC)
- Likelihood Ratio Tests (LRT)

## Key Findings

### Billboard Exposure Analysis
- NBD model significantly outperformed the Poisson model in predicting billboard exposures
- Optimal n value of approximately 0.97 indicated typical exposure patterns before "churn"
- Visual analysis showed higher actual exposures than predicted by Poisson, suggesting effective billboard placement

### Barnes & Noble Website Analysis
- The basic NBD model emerged as the best performer across evaluation metrics
- Reach (proportion of population exposed at least once) calculated at 19.02%
- Average frequency among those exposed was 3.74 visits
- Gross Rating Points (GRP) calculated at 71.1

### Customer Characteristics Impact
- Age showed a positive correlation with purchase probability (coefficient ≈ 0.028)
- Income demonstrated positive influence on website visits (coefficient ≈ 0.017)
- Households with children showed higher likelihood of visits (coefficient ≈ 0.059)
- Regional and racial factors showed varied influences on purchasing patterns

## Technical Implementation
- Implemented all models in Python using numerical optimization techniques
- Employed scipy's optimization functions to perform Maximum Likelihood Estimation
- Created data visualization to compare actual vs. predicted values
- Calculated marketing metrics (reach, frequency, GRP) based on model outputs

## Usage
The main analysis is contained in `project-I-group11.ipynb`. To run this analysis:

1. Ensure you have the required dependencies installed:
```
pip install pandas numpy scipy matplotlib seaborn
```

2. Run the Jupyter notebook:
```
jupyter notebook project-I-group11.ipynb
```

3. The notebook contains detailed code and explanations for each modeling approach.

## Skills Demonstrated
- **Statistical Modeling**: Implementation of Poisson and NBD distributions
- **Machine Learning**: Regression modeling with customer characteristics
- **Maximum Likelihood Estimation**: Parameter optimization techniques
- **Data Manipulation**: Transformation and preparation of datasets
- **Hypothesis Testing**: Formal comparison of nested models
- **Business Intelligence**: Extraction of managerial insights from technical results
- **Data Visualization**: Graphical comparison of model performance
