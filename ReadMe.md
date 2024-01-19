# Project Readme

## 1. Introduction

### 1.1 Background
As a Master's student in the last semester, I am actively applying for jobs and am curious to understand:

1. How the hiring process works and which factors are most important for candidates to be called for an interview.
2. Can a machine learning model be developed to accurately predict whether a person would be called for an interview based on specific features?

This project aims to explore and address these questions.

### 1.2 Objectives
The objectives of this project are as follows:

1. Identify factors/features that are crucial for a candidate to be called for an interview.
2. Investigate whether a machine learning model can accurately predict whether a person would be called for an interview based on the identified important features.

## 2. Data Exploration

### 2.1 Data Collection
The dataset used for this project is sourced from Kaggle, titled [HR Competency Scores for Screening](https://www.kaggle.com/datasets/muhammadjawwadismail/hr-competency-scores-for-screening). This dataset was chosen due to its diversity in features and a sufficient number of observations, making it suitable for addressing the project's objectives.

### 2.2 Data Visualization
After loading the relevant libraries and reading the dataset, initial data exploration involves visualizing the distribution of features through box plots. Additionally, a bar plot is used to display the percentages of candidates called for interviews.

## 3. Data Preparation

### 3.1 Data Transformation
Since all features have numerical values, and even the categorical variable "call_for_interview" is represented numerically (1 for "Yes," 0 for "No"), no data transformation is required.

### 3.2 Data Cleaning
Data cleaning involves checking for duplicates, handling missing values, and addressing outliers. In this dataset, no missing values were found, and outliers in the "functional_competency_score" were removed.

### 3.3 Feature Selection
Highly correlated features are identified and addressed to avoid redundancy. The correlation matrix is visualized to understand the relationships between features.

## 4. Model Training

Nine classification models are trained, including KNeighborsClassifier, SVC, NuSVC, DecisionTreeClassifier, RandomForestClassifier, GaussianNB, LinearDiscriminantAnalysis, QuadraticDiscriminantAnalysis, and LogisticRegression. Evaluation metrics such as accuracy, log loss, and F1 score are used to compare the models. Logistic Regression and Quadratic Discriminant Analysis are identified as top-performing models.

## 5. Feature Importance

Logistic Regression is chosen as the final model for interpreting feature importance. The top three most important features are identified as "years_of_experience," "behavior_competency_score," and "top1_skills_score."

## 6. Conclusion

In conclusion:

- The top three most important features based on which candidates are called for an interview are "years_of_experience," "behavior_competency_score," and "top1_skills_score."
- Logistic Regression achieves approximately 90% accuracy in predicting whether a candidate will be called for an interview.

This project provides valuable insights into the hiring process and demonstrates the potential of machine learning models in predicting interview calls based on specific candidate features.
