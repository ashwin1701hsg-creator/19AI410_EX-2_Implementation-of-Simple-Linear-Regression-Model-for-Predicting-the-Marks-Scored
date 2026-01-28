![WhatsApp Image 2026-01-28 at 1 55 53 PM](https://github.com/user-attachments/assets/edd5e3d1-d213-4511-b17f-d6980b268e02)# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

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
# Import required libraries
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Load the dataset
data = pd.read_csv("data.csv")

# Independent variable (X) and Dependent variable (y)
X = data[['Experience']]   # must be 2D
y = data['Salary']

# Create the Linear Regression model
model = LinearRegression()

# Train the model
model.fit(X, y)

# Predict values
y_pred = model.predict(X)

# Display slope and intercept
print("Slope (m):", model.coef_[0])
print("Intercept (c):", model.intercept_)

# Plot the data and regression line
plt.scatter(X, y)
plt.plot(X, y_pred)
plt.xlabel("Experience")
plt.ylabel("Salary")
plt.title("Simple Linear Regression")
plt.show()
```

## Output:
![WhatsApp Image 2026-01-28 at 1 55 53 PM](https://github.com/user-attachments/assets/6d54465f-d8ad-40e9-8b94-b8a33940566e)




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
