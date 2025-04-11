# Advanced Customer Analytics Using MLE

## Project Overview
This repository contains a comprehensive analysis of customer behavior using advanced statistical modeling techniques. The project leverages Maximum Likelihood Estimation (MLE) to develop Poisson and Negative Binomial Distribution (NBD) models for predicting customer exposure and purchase patterns. Both the basic and regression variants are implemented to account for customer heterogeneity and derive actionable business insights.

## Table of Contents
- [Introduction](#introduction)
- [Project Objectives](#project-objectives)
- [Methodology](#methodology)
  - [Data Processing](#data-processing)
  - [Modeling Approach](#modeling-approach)
  - [Model Evaluation](#model-evaluation)
- [Key Findings](#key-findings)
  - [Billboard Exposure Analysis](#billboard-exposure-analysis)
  - [Barnes & Noble Website Analysis](#barnes--noble-website-analysis)
  - [Customer Characteristics Impact](#customer-characteristics-impact)
- [Technical Implementation](#technical-implementation)
- [Usage](#usage)
- [Skills Demonstrated](#skills-demonstrated)

## Introduction
This project applies sophisticated statistical models to predict customer behavior in two key domains:
- **Billboard Exposure Analysis:** Modeling the frequency of customer exposure to advertising billboards.
- **Online Retail Behavior Analysis:** Predicting customer visits to Barnes & Noble's website, contrasted with Amazon’s data.

The analysis employs both Poisson and NBD models (including their regression variants) to address the inherent heterogeneity in customer responses and generate nuanced forecasts.

## Project Objectives
- **Model Implementation:** Develop and compare Poisson and NBD models to predict count data.
- **Regression Analysis:** Integrate customer-specific variables (age, income, household size, etc.) into Poisson and NBD regression models.
- **Performance Evaluation:** Use evaluation metrics such as Log-Likelihood, AIC, BIC, and Likelihood Ratio Tests (LRT) to assess model fit.
- **Insight Generation:** Extract actionable business insights for optimizing marketing strategies and customer engagement.
- **Behavior Prediction:** Forecast future customer exposure and purchasing patterns based on historical data.

## Methodology

### Data Processing
- **Transformation:** Raw data were transformed into formats suitable for the various modeling approaches.
- **Cleaning:** Systematic cleaning was applied to handle missing values and outliers.
- **Dataset Creation:** Specialized datasets (e.g., `books01.csv` and `books02.csv`) were created to support different analytical methods.

### Modeling Approach
1. **Poisson Model:**  
   - Assumes a constant exposure probability across customers.
   - Applied to both billboard exposures and website visits.
   - Optimized using MLE to estimate the λ parameter.
2. **NBD Model:**  
   - Accounts for heterogeneity in customer behavior with parameters for both purchase intensity (n) and customer “churn” (α).
   - Better models overdispersion commonly observed in count data.
3. **Poisson Regression:**  
   - Integrates customer demographics (e.g., age, income, household size) to customize predictions.
4. **NBD Regression:**  
   - Combines the benefits of the NBD model with regression techniques to incorporate customer characteristics, offering the most robust predictive insights.

### Model Evaluation
Models were assessed using:
- **Log-Likelihood:** As a measure of model fit.
- **AIC and BIC:** To balance model fit with complexity.
- **Likelihood Ratio Tests (LRT):** For formal comparisons between nested models.

## Key Findings

### Billboard Exposure Analysis
- The NBD model significantly outperformed the Poisson model in predicting billboard exposures.
- An optimal n value of approximately 0.97 indicates typical customer exposure patterns before a “churn” event.
- Graphical analyses suggested that actual exposures were higher than Poisson predictions, pointing to effective billboard placements.

### Barnes & Noble Website Analysis
- The NBD model emerged as the top performer across evaluation metrics.
- **Reach:** Approximately 19.02% of the target population was estimated to have visited the website at least once.
- **Average Frequency:** Customers visited on average 3.74 times.
- **Gross Rating Points (GRP):** Calculated at 71.1, combining reach and frequency.

### Customer Characteristics Impact
- **Age:** Positive correlation with purchase probability (coefficient ≈ 0.028).
- **Income:** Positive influence on website visits (coefficient ≈ 0.017).
- **Households with Children:** Higher likelihood of visits (coefficient ≈ 0.059).
- **Other Factors:** Regional and racial demographics contributed to varied purchasing patterns.

## Technical Implementation
- Models were implemented in Python using numerical optimization techniques.
- Utilized Scipy's optimization functions to perform Maximum Likelihood Estimation.
- Visualizations were generated to compare actual versus predicted values.
- Calculated key marketing metrics (reach, average frequency, GRP) from model outputs.

## Usage
The core analysis is provided in the Jupyter Notebook: `project-I-group11.ipynb`. To run the analysis locally, follow these steps:

1. **Install Dependencies:**
   ```bash
   pip install pandas numpy scipy matplotlib seaborn
   ```
2. **Run the Notebook:**
   ```bash
   jupyter notebook Advance Customer Analytics.ipynb
   ```
The notebook follows a Q&A format, detailing the code and explanations for each modeling approach.

## Skills Demonstrated
- **Statistical Modeling:** Implementation of Poisson and NBD models.
- **Machine Learning & Regression:** Integration of customer-specific variables for enhanced predictions.
- **Maximum Likelihood Estimation:** Advanced parameter optimization techniques.
- **Data Manipulation:** Effective data cleaning and transformation processes.
- **Hypothesis Testing:** Conducted formal tests to compare nested models.
- **Business Intelligence:** Extraction of actionable insights and marketing KPIs.
- **Data Visualization:** Graphical comparison of model performance.
