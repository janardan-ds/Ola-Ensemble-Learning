# OLA - Ensemble Learning

## Business Case

### Problem Statement

Recruiting and retaining drivers is a significant challenge for Ola. High churn rates among drivers impact the company's operations and increase costs due to frequent recruitment. The objective is to predict whether a driver will leave the company based on various attributes, such as demographics, tenure information, and historical performance data.

### Dataset

The dataset contains monthly information for a segment of drivers for 2019 and 2020. The goal is to use this data to build a predictive model for driver attrition.

- **Columns**:
  - `MMMM-YY`: Reporting Date (Monthly)
  - `Driver_ID`: Unique ID for drivers
  - `Age`: Age of the driver
  - `Gender`: Gender of the driver (Male: 0, Female: 1)
  - `City`: City Code of the driver
  - `Education_Level`: Education level (0: 10+, 1: 12+, 2: Graduate)
  - `Income`: Monthly average Income of the driver
  - `Date Of Joining`: Joining date for the driver
  - `LastWorkingDate`: Last date of working for the driver
  - `Joining Designation`: Designation of the driver at the time of joining
  - `Grade`: Grade of the driver at the time of reporting
  - `Total Business Value`: Total business value acquired by the driver in a month (negative indicates cancellation/refund or car EMI adjustments)
  - `Quarterly Rating`: Quarterly rating of the driver (1 to 5, higher is better)

## Concepts Tested

- Ensemble Learning: Bagging, Boosting
- KNN Imputation of Missing Values
- Working with an imbalanced dataset

## Steps to Follow

### Data Import and Exploration

1. **Import the Dataset**: Load the dataset and perform initial exploratory data analysis (EDA).
2. **Convert Date Features**: Convert date-like features to appropriate data types.
3. **Check for Missing Values**: Identify and prepare data for KNN imputation, focusing on numerical features.
4. **Aggregate Data**: Remove multiple occurrences of the same driver data by aggregating on `Driver_ID`.

### Feature Engineering

1. **Quarterly Rating Increase**: Create a column indicating whether the quarterly rating has increased (`1` if increased).
2. **Target Variable Creation**: Create a column `target` indicating whether the driver has left the company (`1` if `LastWorkingDate` is present).
3. **Monthly Income Increase**: Create a column indicating whether the monthly income has increased (`1` if increased).
4. **Statistical Summary**: Generate a statistical summary of the derived dataset.
5. **Correlation Check**: Analyze correlations among independent variables and their interactions.
6. **One-Hot Encoding**: Apply one-hot encoding to categorical variables.
7. **Class Imbalance Treatment**: Address class imbalance using appropriate techniques.
8. **Standardization**: Standardize the training data.

### Model Building

1. **Ensemble Learning**: Implement Bagging and Boosting methods with hyper-parameter tuning.
2. **Results Evaluation**:
   - Generate a classification report.
   - Plot and analyze the ROC AUC curve.

### Insights and Recommendations

Provide actionable insights and recommendations based on the model's results to help Ola in their driver retention strategy.

## Results Evaluation

- **Classification Report**: Evaluate the performance using precision, recall, f1-score, and support.
- **ROC AUC Curve**: Analyze the ROC AUC curve to assess the model's performance.

## Actionable Insights & Recommendations

Based on the analysis and model predictions, provide insights and recommendations to help Ola improve driver retention and reduce attrition rates.

