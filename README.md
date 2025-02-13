# Modeling Car Insurances

## Overview

This project aims to develop a predictive model to estimate the likelihood of a customer making a claim on their car insurance during the policy period. Commissioned by a fictional car insurance company, the project seeks to optimize pricing strategies and enhance risk assessment capabilities, crucial for maintaining a competitive edge in the large car insurance market.

## Dataset

The dataset, `car_insurance.csv`, includes various customer attributes:

| Column | Description |
|--------|-------------|
| `id` | Unique client identifier |
| `age` | Client's age: <br> <ul><li>`0`: 16-25</li><li>`1`: 26-39</li><li>`2`: 40-64</li><li>`3`: 65+</li></ul> |
| `gender` | Client's gender: <br> <ul><li>`0`: Female</li><li>`1`: Male</li></ul> |
| `driving_experience` | Years the client has been driving: <br> <ul><li>`0`: 0-9</li><li>`1`: 10-19</li><li>`2`: 20-29</li><li>`3`: 30+</li></ul> |
| `education` | Client's level of education: <br> <ul><li>`0`: No education</li><li>`1`: High school</li><li>`2`: University</li></ul> |
| `income` | Client's income level: <br> <ul><li>`0`: Poverty</li><li>`1`: Working class</li><li>`2`: Middle class</li><li>`3`: Upper class</li></ul> |
| `credit_score` | Client's credit score (between zero and one) |
| `vehicle_ownership` | Client's vehicle ownership status: <br><ul><li>`0`: Does not own their vehilce (paying off finance)</li><li>`1`: Owns their vehicle</li></ul> |
| `vehcile_year` | Year of vehicle registration: <br><ul><li>`0`: Before 2015</li><li>`1`: 2015 or later</li></ul> |
| `married` | Client's marital status: <br><ul><li>`0`: Not married</li><li>`1`: Married</li></ul> |
| `children` | Client's number of children |
| `postal_code` | Client's postal code | 
| `annual_mileage` | Number of miles driven by the client each year |
| `vehicle_type` | Type of car: <br> <ul><li>`0`: Sedan</li><li>`1`: Sports car</li></ul> |
| `speeding_violations` | Total number of speeding violations received by the client | 
| `duis` | Number of times the client has been caught driving under the influence of alcohol |
| `past_accidents` | Total number of previous accidents the client has been involved in |
| `outcome` | Whether the client made a claim on their car insurance (response variable): <br><ul><li>`0`: No claim</li><li>`1`: Made a claim</li></ul> |

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
