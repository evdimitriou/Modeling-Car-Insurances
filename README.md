# Modeling Car Insurances

## Overview

This project aims to develop a predictive model to estimate the likelihood of a customer making a claim on their car insurance during the policy period. Commissioned by a fictional car insurance company, the project seeks to optimize pricing strategies and enhance risk assessment capabilities, crucial for maintaining a competitive edge in the large car insurance market.

## Dataset

The dataset, `car_insurance.csv`, includes various customer attributes:

- **id**: Unique client identifier
- **age**: Client's age group
- **gender**: Client's gender
- **driving_experience**: Years the client has been driving
- **education**: Client's level of education
- **income**: Client's income level
- **credit_score**: Client's credit score (0 to 1)
- **vehicle_ownership**: Ownership status
- **vehicle_year**: Year of vehicle registration
- **married**: Marital status
- **children**: Number of children
- **postal_code**: Postal code
- **annual_mileage**: Miles driven annually
- **vehicle_type**: Type of car
- **speeding_violations**: Number of violations
- **duis**: Driving under influence incidents
- **past_accidents**: Previous accidents
- **outcome**: Claim status (0: No claim, 1: Claim)

## Methodology

1. **Data Cleaning and Transformation**: Handled missing values and transformed categorical variables into numerical representations.
   
2. **Exploratory Data Analysis (EDA)**: Analyzed correlations and visualized data distributions to understand feature relationships.

3. **Feature Selection**: Applied logistic regression to assess each feature's predictive power.

4. **Modeling**: 
   - **Logistic Regression**: Tuned using GridSearchCV, achieving an accuracy of 79%.
   - **Random Forest**: Tuned with parameters `max_depth: None`, `min_samples_split: 2`, `n_estimators: 50`, achieving an accuracy of 82%.

5. **Evaluation**: Used confusion matrices and classification reports to evaluate model performance.

## Results

- **Best Feature**: `driving_experience` was identified as the most predictive feature with an accuracy of 77.71%.
- **Model Performance**:
  - Logistic Regression: Precision of 0.92 for "No Claim" and 0.63 for "Claim".
  - Random Forest: Precision of 0.85 for "No Claim" and 0.70 for "Claim".

## Conclusion

The project successfully identified key predictive features and developed models that enhance decision-making processes. The Random Forest model, with its higher accuracy, is recommended for deployment, providing a balance between simplicity and performance. This approach allows the company to start with a straightforward model in production, minimizing the need for complex infrastructure and expertise.

## Visualizations

Confusion matrices and correlation heatmaps are included to provide visual insights into model performance and feature relationships.
