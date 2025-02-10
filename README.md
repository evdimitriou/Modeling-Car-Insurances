# Modeling Car Insurances

This project involves building a predictive model to estimate the likelihood of a customer making a claim on their car insurance during the policy period. The project is commissioned by "On the Road" car insurance company, which seeks to optimize their pricing strategy and improve their risk assessment capabilities. Given the large market for car insurance, accurate prediction models are crucial for maintaining competitive advantage.

## Project Overview

The primary goal of this project is to identify the single most predictive feature from the provided customer dataset that can be used to predict whether a customer will make a claim. The dataset, `car_insurance.csv`, includes various customer attributes such as age, gender, driving experience, education, income, and more.

## Dataset Description

The dataset contains the following columns:

- **id**: Unique client identifier
- **age**: Client's age group
- **gender**: Client's gender
- **driving_experience**: Years the client has been driving
- **education**: Client's level of education
- **income**: Client's income level
- **credit_score**: Client's credit score (between zero and one)
- **vehicle_ownership**: Client's vehicle ownership status
- **vehicle_year**: Year of vehicle registration
- **married**: Client's marital status
- **children**: Number of children the client has
- **postal_code**: Client's postal code
- **annual_mileage**: Number of miles driven by the client each year
- **vehicle_type**: Type of car
- **speeding_violations**: Total number of speeding violations received by the client
- **duis**: Number of times the client has been caught driving under the influence
- **past_accidents**: Total number of previous accidents the client has been involved in
- **outcome**: Whether the client made a claim on their car insurance

## Methodology

1. **Data Cleaning and Transformation**: The dataset is cleaned by handling missing values and transforming categorical variables into numerical representations.

2. **Feature Selection**: Logistic regression models are applied to each feature individually to determine their predictive power regarding the outcome variable (claim or no claim).

3. **Accuracy Evaluation**: The accuracy of each model is calculated, and the feature with the highest accuracy is identified as the best predictor.

4. **Results**: The best feature and its corresponding accuracy are stored in a DataFrame for easy reference.

## Conclusion

The project successfully identifies the most predictive feature for car insurance claims, providing a simple yet effective model that "On the Road" can use to enhance their decision-making process. This approach allows the company to start with a straightforward model in production, minimizing the need for complex infrastructure and expertise.
