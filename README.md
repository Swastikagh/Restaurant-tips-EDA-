# Restaurant Bills & Tipping — Exploratory Data Analysis

## Overview

An exploratory data analysis project using Python to investigate restaurant bills, tipping patterns, party sizes, and differences between meal periods.

## Objectives

* Inspect and clean data using Pandas and NumPy.
* Explore distributions and relationships using visualizations.
* Identify potential outliers using the interquartile range (IQR) method.
* Perform correlation analysis and hypothesis testing.
* Build and evaluate a baseline linear regression model.
* Communicate findings and limitations in plain English.

## Tools

Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, scikit-learn, Jupyter Notebook.

## Methodology

1. Data inspection and cleaning
2. Exploratory data analysis
3. Outlier detection and investigation
4. Correlation analysis
5. Welch's independent two-sample t-test
6. Linear regression and test-set evaluation
7. Business interpretation and limitations

## Key Findings

* Bill and tip relationship: [<img width="574" height="384" alt="image" src="https://github.com/user-attachments/assets/617e4574-556d-45a8-b5c3-8bba50b8907e" />

<img width="684" height="484" alt="image" src="https://github.com/user-attachments/assets/1dd3d735-7859-4856-9608-fc16307acbaf" />

]
* Lunch versus dinner comparison: [
Lunch sample size: 67
Dinner sample size: 176
Mean lunch bill: $17.23
Mean dinner bill: $20.80
Welch t-statistic: -3.044
p-value: 0.00279
Decision: Reject H0 at the 5% significance level.
Interpretation: The sample provides statistical evidence of a difference in mean bills.
Important: statistical significance does not establish causation or business importance.]
* Outlier analysis: 
total_bill	tip	sex	smoker	day	time	size
170	50.81	10.00	Male	Yes	Sat	Dinner	3
212	48.33	9.00	Male	No	Sat	Dinner	4
59	48.27	6.73	Male	No	Sat	Dinner	4
156	48.17	5.00	Male	No	Sun	Dinner	6
182	45.35	3.50	Male	Yes	Sun	Dinner	3
102	44.30	2.50	Female	Yes	Sat	Dinner	3
197	43.11	5.00	Female	Yes	Thur	Lunch	4
142	41.19	5.00	Male	No	Thur	Lunch	5
184	40.55	3.00	Male	Yes	Sun	Dinner	2

* Predictive model: [<img width="684" height="484" alt="image" src="https://github.com/user-attachments/assets/6ca4b58e-ddc3-4fbb-a5ff-a5af94aad62c" />
]
* Business implications: 

1. **Revenue and tipping patterns:** Analyze the relationship between total bills and tips to understand customer tipping behaviour. If the analysis shows a positive correlation, restaurants can use this insight to investigate how spending patterns relate to tips, while recognizing that correlation does not establish causation.

2. **Meal-period planning:** Compare average lunch and dinner bills and review the Welch's t-test results. If dinner bills are meaningfully higher, management could investigate meal-period differences in menu choices, party sizes, and service requirements before making staffing or promotional decisions.

3. **Transaction monitoring and forecasting:** Investigate unusually high or low bills flagged by the IQR method rather than automatically removing them. Evaluate the tip prediction model using its test-set MAE and R² to determine whether it provides a useful baseline for forecasting tips. Additional data on restaurant location, promotions, service ratings, and seasonality could improve future analysis.


## Limitations

This is a small sample dataset. The findings may not generalize to other restaurants. Observed relationships do not establish causation, and outliers require investigation before being treated as errors.

## How to Run

Open `restaurant_tips_eda.ipynb` in Google Colab or Jupyter Notebook and execute the cells from top to bottom.

## Author

Swastika Chakraborty
