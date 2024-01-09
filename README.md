# Jamboree GradAdmit Analysis 

## Business Problem

Jamboree, an education platform, aims to assist students in predicting their chances of admission to top international graduate programs. The goal is to understand the key factors influencing graduate admissions and create a predictive model to estimate an individual's likelihood of admission based on various parameters.

## Approach

### Exploratory Data Analysis (EDA)

1. **Loading and Inspecting the Dataset:**
   - Checked the dataset's structure, characteristics, and meaningful column names.
2. **Handling Duplicate Records and Missing Values:**
   - Checked for duplicates, removed unnecessary identifiers, and handled missing values.
3. **Column Profiling:**
   - Examined the unique values and data types of each column.
4. **Numerical and Categorical Analysis:**
   - Analyzed numerical and categorical variables to gain insights into the distribution and relationships.

### Correlation Analysis

1. **Numerical Variables:**
   - Explored relationships between GRE Score, TOEFL Score, CGPA, and the Chance of Admit.
2. **Categorical Variables:**
   - Examined the impact of variables like Research, University Rating, LOR, and SOP on the Chance of Admit.
3. **Multicollinearity Check:**
   - Checked for multicollinearity among independent variables.

### Model Building - Linear Regression

1. **Handling Categorical Variables:**
   - Used pandas Dummies to convert categorical variables to numerical variables.
2. **Backward Elimination for Feature Selection:**
   - Iteratively removed insignificant features based on p-values.
3. **Model Evaluation:**
   - Checked assumptions of linear regression, including multicollinearity, residuals, homoscedasticity, and normality.
4. **Performance Metrics:**
   - Evaluated the model using metrics like MAE, RMSE, R2, and Adjusted R2.

## Observations from Results

1. **Exploratory Data Analysis:**
   - No outliers were observed in GRE Score, TOEFL Score, and CGPA.
   - Research is evenly distributed, and a majority of students have a university rating of 3 or 2.
   - Positive relationships exist between Chance of Admit and numerical variables.
   - Strong correlations were found between GRE Score, TOEFL Score, and CGPA.

2. **Linear Regression Model:**
   - The final model includes significant predictors like GRE Score, LOR_4.0, LOR_4.5, and LOR_5.0.
   - R2 value indicates a good fit, but there is room for improvement.
   - Assumptions like multicollinearity, residuals, and homoscedasticity were validated.

## Recommendations

1. **Feature Improvement:**
   - Explore additional features like GRE_TOEFL_CGPA_Ratio for potential model enhancement.
   - Consider handling outliers more effectively.

2. **Model Enhancement:**
   - Experiment with non-linear models for potential improvements.
   - Evaluate the impact of other variables or interactions not considered in the current model.

3. **Usage Suggestions:**
   - Implement the model on Jamboree's platform for students to predict their admission chances.
   - Highlight key factors influencing admission, such as GRE Score, TOEFL Score, CGPA, and strong Letters of Recommendation.

## Conclusion

The analysis provides valuable insights into graduate admission factors and establishes a predictive model. While the current model is robust, there are opportunities for enhancement. Understanding the importance of features and continually refining the model can significantly benefit students in predicting their chances of admission.
