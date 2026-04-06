# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import required libraries and load the dataset from the CSV file.
2. Separate the dataset into independent variable (Experience) and dependent variable (Salary).
3.Create the Linear Regression model and train it using the given data.
4.Predict the salary values, display slope and intercept, and plot the regression line with the data points.
## Program:
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
import numpy as np

raw_data = {
    'Hours': [12, 16, 18, 22, 24, 32, 37, 38, 40, 42],
    'Marks': [30, 37, 47, 54, 60, 63, 68, 78, 84, 92]
}
data = pd.DataFrame(raw_data)

X = data[['Hours']]  
y = data['Marks']       

model = LinearRegression()
model.fit(X, y)

y_pred = model.predict(X)

m = model.coef_[0]
c = model.intercept_

print(f"Slope (m): {m:.2f}")
print(f"Intercept (c): {c:.2f}")
print(f"Equation: Marks = {m:.2f} * Hours + {c:.2f}")

plt.figure(figsize=(10, 6))
plt.scatter(X, y, color='blue', label='Actual Data')
plt.plot(X, y_pred, color='red', linewidth=2, label='Regression Line')
plt.xlabel("Hours Spent")
plt.ylabel("Marks Achieved")
plt.title("Simple Linear Regression: Hours vs Marks")
plt.legend()
plt.grid(True, linestyle='--', alpha=0.6)
plt.show()


```
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: ASHWIN H
RegisterNumber: 212225230025
*/
```
## Output:
![WhatsApp Image 2026-01-28 at 1 55 53 PM](https://github.com/user-attachments/assets/6d54465f-d8ad-40e9-8b94-b8a33940566e)




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
