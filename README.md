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
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LogisticRegression

# Dataset: marks vs result
X = np.array([[30], [35], [40], [45], [50], [55], [60], [65]])
y = np.array([0, 0, 0, 0, 1, 1, 1, 1])   # 0 = Fail, 1 = Pass

# Create and train model
model = LogisticRegression()
model.fit(X, y)

# Predict for a new student
marks = [[48]]
result = model.predict(marks)
print("Prediction (0=Fail, 1=Pass):", result)

# Plot data points
plt.scatter(X, y, color='red', label='Actual Data')

# Plot logistic regression curve
X_test = np.linspace(25, 70, 100).reshape(-1, 1)
plt.plot(X_test, model.predict_proba(X_test)[:,1], label='Prediction Curve')

plt.xlabel("Marks")
plt.ylabel("Probability of Pass")
plt.title("Logistic Regression: Pass / Fail Prediction")
plt.legend()
plt.show()
```

## Output:
![WhatsApp Image 2026-01-28 at 1 55 53 PM](https://github.com/user-attachments/assets/6d54465f-d8ad-40e9-8b94-b8a33940566e)




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
