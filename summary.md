
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

#### Algorithm
A linear regression model was used to predict the average_scores of students.
see linear_model.joblib

#### Preprocessing
- I dropped duplicates as they were disruptive.
- **Categorical features** such as `gender`, `race/ethnicity`, `parental level of education`, `lunch`, `test preparation course` where one-hot encoded and also standardized to eliminate multicollinearity.


---

### Evaluation 

#### Metrics
-`Mean Squared Error(mse)`: 149.88
-`Mean Absolute Error`: 9.5876
-`R2 Score`: 0.2867
-`Root Mean Squared Error (rmse)`` : 11.959 below the rmse baseline of 22.2

#### Feature Importance

-`lunch`,`test_preparation_course` were the most influential predictors of students' performance.

---

## Analysis Results 

**See visualizations.pdf for the visualizations**

### How does each feature correlate with the students' average scores? 
(see correlation map in `visualizations.pdf`)
1. **Positively Correlated Features:**
   - `lunch_standard` (0.29): Strongest positive correlation; indicates that students with standard lunches tend to have higher scores.
   - `ethnicity_group E` (0.15): Slight positive correlation.
   - `parental_level_of_education_bachelor's degree` (0.12): Slight positive correlation.
   - `parental_level_of_education_master's degree` (0.057): Minimal positive correlation.
   - `parental_level_of_education_some_college` (0.035): Very minimal positive correlation.

2. **Negatively Correlated Features:**
   - `test_preparation_course_none` (-0.26): Strongest negative correlation; students who did not take test prep tend to score lower.
   - `parental_level_of_education_high school` (-0.17): Negative correlation.
   - `gender_male` (-0.13): Males slightly tend to score lower.
   - `ethnicity_group B` (-0.11): Slight negative correlation.
   - `parental_level_of_education_some_high school` (-0.064): Minimal negative correlation.
   - `ethnicity_group C` (-0.029): Very weak correlation (near zero).

#### Conclusion:
- **Lunch type** and **test preparation** are the most influential features.
- **Parental education** has minimal impact, except for bachelor's degrees.
- **Ethnicity groups C and D** and **gender** have negligible effects on scores.

### What are the most important factors that influence students' grades?

**see `visualizations.pdf` for the feature importance bar plot**

**Top Three**

1. **`lunch_standard`**: This feature has the highest importance, suggesting its significant influence on average scores.  
2. **`test_preparation_course_none`**: Strongly impacts scores negatively. That student with no preparation performed less as compared to the ones who did.  
3. **`ethnicity_group E`**: Moderate positive impact. 
