# NPL-Recovery-Prediction
# Non Performing Loans Recovery Prediction

## Project Overview

This project analyzes non-performing loan customers and ranks them based on their likelihood of recovery. The goal is to help portfolio managers identify customers with higher recovery potential and support better collection strategies.

## Dataset

The dataset used is `npl_sorted.csv`, which contains customer-level recovery information.

### Columns

- `COD_TIPO_NDG`: Customer type/category code
- `ID_CUSTOMER`: Unique customer identifier
- `IMP_GBV`: Gross Book Value / outstanding debt amount
- `PRED_PROB_RECOVERY_12M_AHEAD`: Predicted probability of recovery within 12 months
- `PRED_RECOVERY_RATE_12M_AHEAD`: Predicted recovery rate within 12 months
- `PRED_INCASSI_12M_AHEAD`: Predicted collections within 12 months
- `PRED_RECOVERY_CLASS`: Predicted recovery category

## Project Steps

1. Load dataset
2. Explore dataset structure
3. Check missing values
4. Check duplicate customers
5. Analyze recovery class distribution
6. Analyze gross book value
7. Analyze predicted recovery probability
8. Perform correlation analysis
9. Detect outliers
10. Create new features
11. Train Random Forest model
12. Evaluate model performance
13. Rank customers by recovery score
14. Export final recovery ranking

## Feature Engineering

Three new features were created:

- `expected_recovery_ratio`
- `unrecovered_amount`
- `recovery_score`

## Model Used

A Random Forest Classifier was used because it performs well on tabular data and provides feature importance.

## Business Recommendation

Customers with higher recovery scores should be prioritized for collection efforts because they show stronger recovery potential.

Customers with medium scores may be targeted with restructuring offers or reminder campaigns.

Customers with low scores may require manual review, legal recovery, or long-term monitoring.

## Limitation

The available dataset does not contain a date or month column. Therefore, seasonality and monthly trend analysis could not be performed.

## Future Work

Future improvements may include:

- Adding original monthly account-level data
- Creating a time-based target variable
- Comparing multiple machine learning models
- Adding customer demographic and guarantee information
- Building a dashboard for portfolio managers
