
# Grade Factor Challenge Summary 

## Overview

I analyzed a dataset to identify factors influencing students' grades. Using various attributes to predict and analyze students' average scores.

---
### Dataset Information

- **Source:** [Kaggle](https://www.kaggle.com/spscientist/students-performance-in-exams)
- **Columns:**
  - `gender`, `race/ethnicity`, `parental level of education`, `lunch`, `test preparation course`, and `average_score`.
  - 
**Key Features**
The significant features used in this model were `gender`, `ethnicity`, `parental_level_of_education`, `lunch`, `test preparation course`


**Target Variable**

- The model is built to predict students' average scores using the provided features.


---
## Model Description 
**Algorithm**
A linear regression model was used to predict the average_scores of students.
see linear_model.joblib

**Preprocessing**
- I dropped duplicates as they were disruptive.
- Categorical features such as `gender`, `race/ethnicity`, `parental level of education`, `lunch`, `test preparation course` where one-hot encoded and also standardized to eliminate multicollinearity.


---
### Evaluation 
**Metrics**
-Mean Squared Error(mse): 149.88
-Mean Absolute Error: 9.5876
-R2 Score : 0.2867
-Root mse : 11.959 below the rmse baseline of 22.2
**Feature Importance**
-`lunch`,`test_preparation_course` were the most significant predictors of student performance.

---

### Findings
**See visualizations.pdf for the findings**
-`lunch_standard` had the highest correlation with the average_scores. see the heatmap in visualizations.pdf for more
-Those who had no `test_preparation_course` had the highest negative correlation signifying that Students who were not tested perfomed worse.
-`parental_level_of_education` had the most minimal effect on the `average_scores`

