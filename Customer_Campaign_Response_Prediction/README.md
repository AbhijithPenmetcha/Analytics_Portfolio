# Customer Campaign Response Prediction Using Machine Learning

**Python | Predictive Analytics | Customer Segmentation | Marketing Analytics**

## Project Overview

A retail superstore is preparing a promotional campaign for its Gold Membership program, offering customers a discounted membership price of $499.

The business challenge is determining which customers are most likely to respond positively to the offer. Contacting every customer increases marketing costs, while overly restrictive targeting risks missing potential conversions.

This project analyzes customer demographics, purchasing behavior, and historical campaign engagement to develop machine learning models that can support more informed marketing decisions.

## Business Objectives

- Identify customer characteristics associated with campaign response.
- Explore purchasing behavior and engagement patterns.
- Build and compare classification models to predict customer responses.
- Address class imbalance using SMOTE.
- Evaluate model performance using accuracy, precision, recall, and F1-score.
- Recommend targeting strategies that balance conversion opportunities with outreach costs.

## Tools and Technologies

- **Programming:** Python
- **Data Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Class Imbalance:** SMOTE (Imbalanced-learn)
- **Development Environment:** Google Colab

## Analytical Approach

### 1. Exploratory Data Analysis

Examined customer demographics, income, household characteristics, product spending, and historical campaign engagement to understand differences between responders and non-responders.

### 2. Data Preparation and Feature Engineering

Handled missing values, transformed categorical features, developed customer-level attributes, and prepared the dataset for classification modeling.

### 3. Predictive Modeling

Implemented and compared multiple machine learning approaches:

- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Voting Classifier

SMOTE was explored to address the imbalance between campaign responders and non-responders.

### 4. Model Evaluation

Compared classification performance with particular attention to positive-class recall and precision, rather than relying solely on overall accuracy.

## Key Results

The analysis revealed that models with high overall accuracy did not necessarily identify a large proportion of actual campaign responders.

| Model | Accuracy | Responder Precision | Responder Recall |
|---|---:|---:|---:|
| Logistic Regression | 87% | 61% | 27% |
| Logistic Regression + SMOTE | 76% | 34% | 68% |
| Random Forest | 87% | 58% | 32% |
| Random Forest + SMOTE | 85% | 48% | 45% |
| Voting Classifier | 82% | 40% | 58% |

*Results reflect the original notebook's reported test evaluations. They are exploratory and should be interpreted in light of the validation limitations discussed below.*

**Key observations:**

- Logistic Regression with SMOTE achieved the highest responder recall among the compared approaches, identifying 68% of actual responders.
- Random Forest with SMOTE offered a comparatively balanced precision-recall trade-off.
- The Voting Classifier demonstrated competitive recall while maintaining moderate precision.
- Total spending, income, and recency emerged as influential features in the Random Forest analysis.

## Business Recommendations

**1. Prioritize responder identification rather than accuracy alone.**

A model that correctly classifies most non-responders may still miss customers likely to accept the membership offer. Marketing teams should evaluate recall alongside precision.

**2. Select a model based on marketing costs and campaign objectives.**

When contacting non-responders is expensive, precision becomes more important. When missing potential conversions is more costly, the business may prioritize recall.

**3. Use customer behavior to inform segmentation.**

Purchasing patterns, income, and recency can support customer segmentation and further targeting experiments. These relationships should be validated before making operational targeting decisions.

**4. Validate before operational deployment.**

Further evaluation should address preprocessing and model-selection limitations, assess performance on untouched data, and incorporate actual campaign economics.

## Limitations and Future Scope

- The analysis uses historical customer data and does not establish causal effects.
- Some preprocessing and model-selection decisions require additional validation to eliminate potential data leakage.
- Actual marketing costs, contribution margins, and incremental campaign effects are unavailable.
- Future improvements could include leakage-safe cross-validation, probability-threshold optimization, campaign economics, and prospective testing.

## Project Notebook

[View the full Python analysis](Customer_Campaign_Response_Prediction.ipynb)

## Author

**Abhijith Penmetcha**

[LinkedIn](https://www.linkedin.com/in/abhijith-penmetcha/)

*Portfolio project demonstrating the application of predictive analytics to customer targeting and business decision-making.*
