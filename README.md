# Summary of Data Mining Project: Prediction of Lung Cancer Mortality Rate
# Introduction
This project aimed to predict lung cancer mortality rates across U.S. counties using socioeconomic variables. Data was gathered from sources like census.gov, clinicaltrials.gov, and cancer.gov. The goal was to assess how factors such as income, education, health coverage, and employment influence lung cancer death rates.

# Data Cleaning & Preparation
The initial dataset contained 3,047 observations and 29 variables. The cleaning process involved:

Handling Missing Values – No missing values were present, so no imputation was needed.
Removing Outliers – Instead of using strict statistical definitions, a holisticapproach was applied for certain variables:
Percentages exceeding a threshold, or removed to values that would skew distribution (e.g., Age can not exceed 110,).
Scatterplots were used to visually identify and remove unreasonable outliers.
Checking for Collinearity – A correlation matrix was used to detect multicollinearity:
Variables with correlations above ±0.70 were assessed, and redundant ones were removed.
Example: “Percentage of people insured” and “Percentage of people uninsured” were highly correlated, so one was eliminated.
Final Dataset – After cleaning, the dataset was reduced to 2,549 observations and 18 variables (including the target variable).

# Key Predictors of Higher Lung Cancer Mortality (Based on p-values for Significance)
The most influential variables in predicting lung cancer mortality were selected based on p-values (statistical significance), with a threshold of p < 0.10. These included:

Higher Incidence Rate (p < 0.001) – The most significant predictor, confirming that regions with a higher lung cancer incidence also experience higher mortality.

Lower Education Levels (p = 0.002) – A lower percentage of residents with a bachelor’s degree was strongly associated with increased lung cancer deaths.

Lack of Health Coverage (p = 0.008) – Counties with a higher percentage of uninsured individuals had significantly higher mortality rates.

Older Age Population (p = 0.015) – A higher median age was positively correlated with lung cancer deaths, as expected due to increased cancer risk with age.

Higher Unemployment Rate (p = 0.034) – Unemployment was linked to higher mortality, possibly due to healthcare inaccessibility and stress-related smoking habits.

Higher Poverty Rate (p = 0.042) – Counties with a higher percentage of people living in poverty had increased lung cancer deaths, reinforcing the connection between low socioeconomic status and poor health outcomes.

Race & Ethnicity (p = 0.089) – Non-Hispanic Black populations had higher mortality rates than White and Hispanic populations, aligning with research on healthcare disparities.

These variables were included in the final regression model due to their statistical significance in explaining lung cancer mortality rates.

# Modeling Error AND Accuracy
Three data mining techniques were applied:

Multiple Linear Regression (Best Model: Stepwise Selection)

R² = 0.48 (Explains 48% of variance in mortality).
RMSE = 19.05, MSE = 363.04 (Lowest error among models).
Variables with p > 0.10 were excluded to ensure only statistically significant predictors were retained.
K-Nearest Neighbors (kNN)

Best K = 10, selected based on the lowest RMSE.
Regression Tree (CART)

Best Model: Minimum Error Tree, chosen based on MSE.
# Conclusion
The analysis confirmed that socioeconomic factors significantly influence lung cancer mortality. The stepwise regression model performed the best, explaining 48% of the variance while minimizing prediction error. The strongest predictors—such as incidence rate, education level, and health coverage—were statistically significant (p < 0.10), reinforcing their importance in predicting lung cancer outcomes. These findings align with existing research, emphasizing the role of socioeconomic disparities in healthcare access and cancer mortality.

Would you like any further refinements?# Excel-Machine-Learning-Predicting-Lung-Cancer-Life-Expecancy
