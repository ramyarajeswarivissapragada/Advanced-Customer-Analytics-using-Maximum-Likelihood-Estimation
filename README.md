# Advanced Customer Analytics Using MLE

## Project Overview
This repository contains a comprehensive analysis of customer behavior using advanced statistical modeling techniques. The project leverages Maximum Likelihood Estimation (MLE) to develop Poisson and Negative Binomial Distribution (NBD) models for predicting customer exposure and purchase patterns. Both basic and regression variants are implemented to account for customer heterogeneity and to derive actionable business insights.

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
- [Managerial Insights](#managerial-insights)
- [Technical Implementation](#technical-implementation)
- [Usage](#usage)
- [Skills Demonstrated](#skills-demonstrated)

## Introduction
This project applies sophisticated statistical models to predict customer behavior in two key domains:
- **Billboard Exposure Analysis:** Modeling the frequency of customer exposure to advertising billboards.
- **Online Retail Behavior Analysis:** Forecasting customer visits to Barnes & Noble's website in contrast with Amazon's visit data.

The analysis employs both Poisson and NBD models, including regression variants that incorporate customer characteristics, to generate nuanced forecasts and inform actionable business strategies.

## Project Objectives
- **Model Implementation:** Develop and compare Poisson and NBD models for count data prediction.
- **Regression Analysis:** Incorporate customer-specific variables into Poisson and NBD regression models.
- **Performance Evaluation:** Use metrics such as Log-Likelihood, AIC, BIC, and Likelihood Ratio Tests (LRT) to assess model fit.
- **Insight Generation:** Derive actionable business insights to optimize advertising and digital marketing strategies.
- **Behavior Prediction:** Forecast future customer exposures and purchase patterns based on historical data.

## Methodology

### Data Processing
- **Transformation:** Raw data was transformed into formats suitable for multiple modeling approaches.
- **Cleaning:** Systematic handling of missing values and outliers ensured data integrity.
- **Dataset Creation:** Specialized datasets (e.g., `books01.csv` and `books02.csv`) were prepared for distinct analytical approaches.

### Modeling Approach
1. **Poisson Model:**  
   - Assumes equal exposure probability for all customers.
   - Applied to both billboard exposure and website visit data.
   - Optimized using MLE to estimate the λ parameter.
2. **NBD Model:**  
   - Accounts for customer heterogeneity using parameters for purchase intensity (n) and churn (α).
   - Effectively captures overdispersion in count data.
3. **Poisson Regression:**  
   - Integrates customer demographics (age, income, household size, etc.) to tailor predictions.
4. **NBD Regression:**  
   - Combines NBD’s advantages with regression analysis to incorporate customer characteristics, offering robust predictive insights.

### Model Evaluation
Models were rigorously evaluated using:
- **Log-Likelihood:** To measure model fit.
- **AIC and BIC:** To balance fit with model complexity.
- **Likelihood Ratio Tests (LRT):** For formal comparisons between nested models.

## Key Findings

### Billboard Exposure Analysis
- **Model Performance:** The NBD model significantly outperformed the Poisson model in predicting billboard exposures.
- **Exposure Patterns:** An optimal n value of approximately 0.97 indicated typical customer exposure patterns before the “churn” effect.
- **Graphical Analysis:** Actual billboard exposures were generally higher than Poisson predictions, suggesting successful billboard placements.

### Barnes & Noble Website Analysis
- **Model Selection:** The basic NBD model emerged as the best performer according to evaluation metrics.
- **Key Metrics:**
  - **Reach:** Approximately 19.02% of the target population visited the website at least once.
  - **Average Frequency:** Among those exposed, the average visit frequency was 3.74.
  - **Gross Rating Points (GRP):** Calculated at around 71.1, derived from the combination of reach and frequency.

### Customer Characteristics Impact
- **Age:** Positive correlation with purchase probability (coefficient ≈ 0.028).
- **Income:** Exhibited a positive influence on website visits (coefficient ≈ 0.017).
- **Households with Children:** Showed a higher likelihood of visits (coefficient ≈ 0.059).
- **Other Demographics:** Regional and racial factors demonstrated varied effects on purchasing patterns.

## Managerial Insights
- **Advertising Strategy:**  
  The analysis of billboard exposures reveals that actual customer exposures consistently exceeded Poisson-based predictions. This suggests that investing in high-traffic billboard placements with appealing designs can lead to enhanced reach.  
- **Digital Marketing Optimization:**  
  The website analysis indicates a solid performance with a 19.02% reach and robust visit frequency, highlighting the importance of digital strategies such as SEO, user experience improvement, and targeted online advertising.
- **Customer Engagement and Segmentation:**  
  Regression analyses have underscored that certain demographics (e.g., older age, higher income, households with children) are more likely to engage and purchase. Tailored marketing campaigns focusing on these segments can drive higher conversion rates and boost overall revenue.
- **Strategic Decision-Making:**  
  The systematic comparison of models using AIC, BIC, and LRT ensures that the selected modeling approach is both robust and parsimonious. This rigorous evaluation supports informed managerial decisions related to budget allocation and campaign planning.

## Technical Implementation
- Implemented all models in Python using numerical optimization techniques.
- Employed Scipy’s optimization functions to perform Maximum Likelihood Estimation.
- Visualizations were created to compare actual versus predicted values.
- Calculated key digital marketing metrics (reach, frequency, GRP) derived from model outputs.

## Usage
The main analysis is provided in the Jupyter Notebook: `project-I-group11.ipynb`. To run the analysis locally, follow these steps:

1. **Install Dependencies:**
   ```bash
   pip install pandas numpy scipy matplotlib seaborn
   ```
2. **Run the Notebook:**
   ```bash
   jupyter notebook Advance Customer Analytics using MLE.ipynb
   ```

The notebook is structured in a Q&A format, detailing the code and explanations for each modeling approach.

## Skills Demonstrated
- **Statistical Modeling:** Implementation of Poisson and NBD distributions.
- **Regression Analysis:** Incorporation of customer-specific variables.
- **Maximum Likelihood Estimation:** Advanced parameter optimization techniques.
- **Data Manipulation:** Data cleaning and transformation.
- **Hypothesis Testing:** Use of formal statistical tests to compare models.
- **Business Intelligence:** Translating technical outputs into actionable marketing insights.
- **Data Visualization:** Graphical representation of model performance.
