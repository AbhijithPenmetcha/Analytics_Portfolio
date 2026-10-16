
# Employee Turnover Prediction Using Machine Learning

**Python | Decision Tree Classification | People Analytics | Predictive Modeling**

## Project Overview

Employee turnover can increase recruitment costs, disrupt operations and affect organizational performance. Understanding which employee characteristics are associated with turnover can help organizations investigate retention challenges before they escalate.

This project applies Decision Tree classification to historical employee data to predict turnover and identify patterns related to employee satisfaction, performance, tenure and workload.

## Business Objectives

- Develop a classification model to predict employee turnover.
- Identify employee characteristics associated with turnover.
- Evaluate predictive performance using accuracy, precision, recall and F1-score.
- Examine model decisions to understand important predictors.
- Translate analytical findings into potential workforce retention strategies.

## Dataset & Preprocessing

The original dataset contained 14,999 employee records.

During preprocessing, 3,008 identical records were removed, leaving 11,991 observations for analysis.

The cleaned dataset was divided into:

- **Training set:** 8,993 records
- **Testing set:** 2,998 records
- **Turnover rate:** 16.60%

Categorical variables including salary and department were encoded for modeling.

Because unique employee identifiers were unavailable, identical records were removed as a modeling assumption rather than confirmed duplicate employees.

## Analytical Approach

### 1. Data Preparation

Examined employee attributes, encoded categorical variables and prepared the dataset for classification.

### 2. Decision Tree Modeling

Developed a Decision Tree classifier using Gini impurity with the following parameters:

- Maximum depth: 5
- Minimum samples per leaf: 20
- Train/test split: 75% / 25%

### 3. Model Evaluation

Evaluated the model using a held-out test dataset and five-fold stratified cross-validation.

### 4. Feature Importance

Examined the relative contribution of employee characteristics to understand which variables influenced the model's predictions.

## Model Performance

### Test Set Results

| Metric | Score |
|---|---:|
| Accuracy | 97.93% |
| Precision (Turnover) | 96.19% |
| Recall (Turnover) | 91.16% |
| F1-score (Turnover) | 93.61% |

The model correctly identified **454 of 498 employees who left** in the test dataset.

### Confusion Matrix

| Actual / Predicted | Stayed | Left |
|---|---:|---:|
| Stayed | 2,482 | 18 |
| Left | 44 | 454 |

### Cross-Validation Results

Five-fold stratified cross-validation produced:

| Metric | Average Score |
|---|---:|
| Accuracy | 97.54% |
| Precision | 94.36% |
| Recall | 90.62% |
| F1-score | 92.44% |

The consistency between training, testing and cross-validation results suggests stable performance on this dataset.

## Key Findings

### Most Influential Features

| Feature | Importance |
|---|---:|
| Employee Satisfaction | 52.23% |
| Performance Evaluation | 17.53% |
| Tenure | 12.42% |
| Number of Projects | 11.88% |
| Average Monthly Working Hours | 5.90% |

Employee satisfaction emerged as the strongest predictor of turnover.

The Decision Tree also identified relationships involving performance evaluations, tenure and workload-related characteristics.

These are predictive associations rather than evidence that individual factors directly cause turnover.

## Business Recommendations

**1. Monitor Employee Satisfaction**

Use regular employee feedback and satisfaction assessments to identify potential concerns and opportunities for support.

**2. Investigate Workload Patterns**

Examine project assignments and working hours to identify teams that may benefit from workload adjustments.

**3. Evaluate Tenure-Related Retention Trends**

Analyze turnover patterns across employee tenure groups to understand where additional support may be useful.

**4. Strengthen Performance Conversations**

Combine performance reviews with employee feedback and development discussions to identify opportunities for improving employee experience.

**5. Validate Before Operational Deployment**

Evaluate the model on newer employee data and assess fairness before using predictions to inform workforce decisions.

## Limitations

- The dataset does not contain unique employee identifiers.
- Removing identical records may exclude employees with matching characteristics.
- Historical model performance may not generalize to future employee populations.
- Predictive relationships do not establish causation.
- Real-world applications would require additional validation, privacy protections and fairness assessments.

## Project Notebook

[View the Full Python Analysis](Employee_Turnover_Prediction.ipynb)

## Author

**Abhijith Penmetcha**

[LinkedIn](https://www.linkedin.com/in/abhijith-penmetcha/)
