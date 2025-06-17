# Income-Bias-Analysis
## Introduction
Understanding the factors that influence income is a central question in social science, economics, and business analytics. This analysis explores a comprehensive dataset containing demographic, educational, occupational, and income information for over 32,000 individuals. The primary objective is to uncover the key drivers of high earnings, identify patterns and disparities across different groups, and provide actionable insights for decision-makers.

By leveraging both exploratory data analysis and advanced modeling techniques, this study examines how features such as education, occupation, gender, age, and country interact to shape income potential. Special attention is given to intersectional effects—how combinations of characteristics (e.g., education and gender, occupation and country) jointly impact the likelihood of being a high earner.

The findings from this analysis aim to inform strategies for employers, policymakers, and marketers seeking to promote equity, target high-potential segments, and design effective interventions in workforce development and compensation.
## overview
Data Overview
Rows: 32,561 individuals
Columns: 15 features
## Key Features
Demographics:

age (integer): Age of the individual
sex (categorical): Male or Female
race (categorical): Ethnic background
country (categorical): Country of origin
Socioeconomic:

workclass (categorical): Type of employment (e.g., Private, Self-emp, Government)
fnlwgt (integer): Final weight (census sampling weight)
education (categorical): Highest level of education attained
education-num (integer): Years of education
marital-status (categorical): Marital status
occupation (categorical): Job type
relationship (categorical): Relationship to household head
Financial:

capital-gain (integer): Investment income from capital gains
capital-loss (integer): Losses from investment
hours-per-week (integer): Average hours worked per week
salary (binary integer): Target variable; 1 = high earner, 0 = low earner
Data Quality
No missing values after cleaning.
Numeric features have been capped at the 1st and 99th percentiles to reduce the impact of outliers.
The target variable (salary) is imbalanced: about 24% are high earners.
## Key Metrics
### Dataset Size
Total records: 32,561
Total features: 15
### Target Variable (salary)
High earners (salary=1): 24%
Low earners (salary=0): 76%
Class imbalance: Yes
### Numeric Features (Median, Range)
Feature	Median	Min	Max
age	37	17	74
fnlwgt	178,356	27,186	510,072
education-num	10	3	16
capital-gain	0	0	15,024
capital-loss	0	0	1,980
hours-per-week	40	8	80
### Categorical Features (Top Categories)
workclass: Private (70%), Self-emp-not-inc, Local-gov
education: HS-grad, Some-college, Bachelors
marital-status: Married-civ-spouse, Never-married, Divorced
occupation: Prof-specialty, Craft-repair, Exec-managerial
relationship: Husband, Not-in-family, Own-child
race: White (85%), Black, Asian-Pac-Islander
sex: Male (67%), Female (33%)
country: United-States (90%), Mexico, ?
### Data Quality
Missing values: None (after cleaning)
Outliers: Capped at 1st and 99th percentiles for numeric features
## skills and concept demostrated
### Data Cleaning & Preprocessing
Handling missing values and ensuring data completeness.
Detecting and capping/removing outliers in numeric features.
Encoding categorical variables for analysis and modeling.
### Exploratory Data Analysis (EDA)
Generating descriptive statistics for numeric and categorical features.
Visualizing distributions (histograms, boxplots, violin plots) to understand feature spread and skewness.
Analyzing class imbalance in the target variable.
### Feature Engineering
Creating capped versions of features to handle outliers.
Constructing intersectional features (e.g., education & gender) for deeper insights.
### Segmentation & Group Analysis
Grouping data by key features (e.g., education, occupation, gender, country) to compare high and low earners.
Calculating and visualizing proportions of high earners within each group.
### Intersectional Analysis
Exploring how combinations of features (e.g., education and gender, occupation and country) jointly affect income outcomes.
Using heatmaps and pivot tables for multi-dimensional group comparisons.
### Correlation & Feature Importance
Computing correlation matrices to identify relationships between numeric features and the target.
Using machine learning models (Random Forest) to rank feature importance for predicting high salary.
### Anomaly Detection
Identifying and flagging outliers and anomalies in the data for further review.
### Data Visualization
Creating clear, informative plots (bar charts, heatmaps, scatterplots) to communicate findings.
Using visualizations to highlight disparities and key patterns.
### Actionable Insights & Recommendations
Translating data findings into practical strategies for business, policy, and further analysis.
## visualization and analysis
[download here](http://localhost:8888/notebooks/Untitled48.ipynb)
## insight

### Income Distribution

Only about 24% of individuals are high earners (salary=1), indicating a strong class imbalance.
Key Numeric Drivers

### Higher education (education-num), capital-gain, age, and hours-per-week are strongly associated with higher salary.
Most people have zero capital-gain/loss, but those with nonzero values are much more likely to be high earners.
Categorical Patterns

### Advanced education (Doctorate, Prof-school, Masters) dramatically increases the likelihood of high earnings.
Professional and managerial occupations (Exec-managerial, Prof-specialty) have the highest proportions of high earners.
Being married (especially Married-civ-spouse) is associated with higher income.
Males are nearly three times as likely as females to be high earners, even after controlling for education and occupation.
Intersectional Effects

### The combination of education and gender, or occupation and country, has a compounding effect on income potential.
Gender gaps persist at every education level, but narrow at the highest degrees.
Some countries (e.g., Iran, France, India) have higher proportions of high earners in certain occupations, but the US dominates the data.
Feature Importance

### Both numeric and categorical features are important for predicting high salary, with education, occupation, and relationship status among the top predictors.
Data Quality

### No missing values after cleaning.
### Outliers in numeric features have been capped to reduce their impact.
## Recommendations
### For Employers & HR:

Promote advanced education and professional development for all employees to increase earning potential.
Address gender disparities in high-earning roles through mentorship, pay equity audits, and transparent promotion criteria.
Target recruitment and retention efforts toward high-potential groups (e.g., women with advanced degrees, young professionals in managerial tracks).
### For Marketers & Business Strategists:

Segment and target high earners using a combination of education, occupation, and gender.
Localize offerings for high-earning segments in different countries, considering occupation and education patterns.
### For Policymakers & Educators:

### Invest in education and upskilling programs, especially for underrepresented groups.
Encourage diversity and inclusion in high-earning occupations and leadership roles.
### For Data Users & Analysts:

### Use robust statistics and monitor for outliers to ensure data quality.
Address class imbalance in predictive modeling (e.g., with stratified sampling or class weights).
Regularly analyze intersectional effects to uncover hidden disparities and opportunities.
## Conclusion
This analysis reveals that high income is strongly linked to advanced education, professional occupations, and being male, with significant disparities persisting even among the most educated. Intersectional analysis shows that combining education, occupation, and gender provides the most accurate picture of income potential. To maximize opportunity and equity, organizations should focus on promoting advanced education, supporting women and underrepresented groups in high-earning roles, and using data-driven segmentation for targeted strategies. Continuous monitoring and intersectional analysis will ensure that interventions remain effective and inclusive.
