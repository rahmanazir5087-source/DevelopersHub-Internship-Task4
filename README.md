# DevelopersHub-Internship-Task4
whats the description00:47Claude responded: Predicting medical insurance charges using Linear Regression on 1,338 patient records.Predicting medical insurance charges using Linear Regression on 1,338 patient records. Model achieved an R² of 0.784. Smoking status was the dominant cost driver, adding an estimated $23,651 to annual charges. 
# Predicting Insurance Claim Amounts

Part of the Data Science & Analytics Internship at DevelopersHub Corporation (Task 4).

## Objective

Estimate a customer's annual medical insurance charges based on personal details like age, BMI, smoking status, and number of children.

## Dataset

Medical Cost Personal Dataset, 1,338 records with 7 columns. Target column is `charges` (annual insurance cost in USD). No missing values.

## Approach

- Explored the distribution of charges and how each feature relates to cost
- Label encoded `sex` and `smoker` (two categories each)
- One-hot encoded `region` (four categories)
- Split data 80/20 into training and test sets
- Trained a Linear Regression model on the training set
- Evaluated performance using MAE, RMSE, and R²
- Visualized actual vs predicted charges and feature coefficients to interpret results

## Results

| Metric | Value |
|---|---|
| MAE (Mean Absolute Error) | $4,181 |
| RMSE (Root Mean Squared Error) | $5,796 |
| R² Score | 0.784 |

The model explains about 78% of the variation in insurance charges.

## Key insights

- Smoking status is by far the strongest predictor, the model assigns a coefficient of roughly $23,651 to being a smoker, meaning smokers are predicted to pay about $23,651 more per year than non-smokers all else being equal
- BMI, age, and number of children all contribute positively to predicted charges but with much smaller effect sizes
- The model underpredicts for the highest-cost patients, which is a known limitation of linear regression when relationships are non-linear
- Sex and region have minimal impact on the prediction

## Files

- `Insurance_Claim_Prediction.ipynb` - full notebook (EDA, modeling, evaluation, interpretation)
- `insurance_data.csv` - dataset used

## Tools

Python, pandas, matplotlib, seaborn, scikit-learn
