# Simple Linear Regression:
An analysis of the quality of the regression is carried out



<p align="center">
    <img src="https://raw.githubusercontent.com/aplatag/project_SL_regression_quality/main/images/RlinealMW.jpeg" alt="methodology" width="500" >
</p>


## Table of Contents
- [Simple Linear Regression Assumptions](#Simple-Linear-Regression-Assumptions)
- [Simple linear regression Quality](#Simple-linear-regression-Quality)
- [Installation](#installation)
- [Code Example](#code-example)



## Simple Linear Regression Assumptions:
1.  **Outlier**:
The term anomaly indicates that there is data that deviates significantly from the rest.
2. **Normality**:
refers to the normal distribution of errors or residuals.
3. **Homoscedasticity**:
 is another simple linear regression assumption and indicates whether the variance of the residuals is the same across different groups in the database.
4. **Independence**:
 refers to the absence of temporal correlation between residuals.
5. **Linearity**:
 is associated with the presence of a constant change of the variable to be predicted with respect to the predictor.

## Simple linear regression Quality


## Installation

Instructions on how to install the project. For example:
```bash

pip install sl-regression-quality
```
## Code Example
For instance, the following code can be executed in Google Colab. Simply copy and paste it into a new Colab notebook.
```bash

#--------------------------------------------------------------------------------
# 1) Load libraries:
import pandas as pd
from sl_regression_quality.main_routine import regression_quality
from sl_regression_quality.load_data import load_csv

#--------------------------------------------------------------------------------
# 2) Load data

dataset = pd.read_csv('Data_carne_new.csv') # your data
df = pd.read_csv('pruebaResolu.csv') # your data

alpha = 0.05 # significance level
dL = 1.055 # dL

# Total:
x=dataset.iloc[:27,1:2].values
y=dataset.iloc[:27,2:3].values
y_res = df.iloc[:,3:6].values
#--------------------------------------------------------------------------------
# 3) Run analysis
regression_quality(x,y,alpha,dL,y_res)

```
