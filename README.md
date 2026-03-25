# Implementation of Multivariate Linear Regression
# Devoloped by: Chidroop M J, B.Tech.,AIML.
# Registered number: 212225240029
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner / Jupyter notebook.
## Algorithm:
### Step1
import pandas as pd.
### Step2
Read the csv file.
### Step3
Get the value of X and y variables
### Step4
Create the linear regression model and fit.
### Step5
Perdict the Train data and testing data

## Program:
```py
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("cars.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```
## Output:
```text
Coefficients: [0.00755095 0.00780526]
Intercept: 79.69471929115939
Predicted CO2 for the corresponding weight and volume: [114.75968007]
```
### output
<img width="1695" height="487" alt="image" src="https://github.com/user-attachments/assets/daf2148f-7198-4411-bfc7-669eb254456a" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
