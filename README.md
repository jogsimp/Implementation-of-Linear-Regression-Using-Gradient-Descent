# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the dataset, select the independent variable (R&D Spend) and the dependent variable (Profit), and perform feature scaling to standardize the input values.
2. Set up the model parameters (slope m and intercept c) along with the gradient descent hyperparameters such as learning rate and total iterations.
3. Generate predictions using the current parameter values, compute the gradients for both m and c, and update them repeatedly through gradient descent.
4. Display the cost value during the initial iterations, and finally present the optimized slope, intercept, and the predicted profit for all data points.

## Program:
```
/*
Program to implement the linear regression using gradient descent.

import pandas as pd
import numpy as np

df = pd.read_csv("Startups.csv")

X = df["R&D Spend"].values.astype(float)
Y = df["Profit"].values.astype(float)

X = (X - X.mean()) / X.std()

m = 0 
c = 0  
alpha = 0.01
iterations = 1000

n = len(X)

for i in range(iterations):
    y_pred = m * X + c

    dm = (-2/n) * sum(X * (Y - y_pred))
    dc = (-2/n) * sum(Y - y_pred)

    m = m - alpha * dm
    c = c - alpha * dc

    if i <= n:
        cost = (1/n) * sum((Y - y_pred) ** 2)
        print("Iteration {}, Cost={:.4f}, m={:.4f}, c={:.4f}".format(i, cost, m, c))


print("")
print("Final Slope (m):", m)
print("Final Intercept (c):", c)

final_predictions = m * X + c
print("\nPredicted Profit:\n", final_predictions)

Developed by: Joshua Abraham Philip A
RegisterNumber: 25013744
*/
```

## Output:
<img width="338" height="595" alt="Screenshot 2025-12-04 at 9 57 29 PM" src="https://github.com/user-attachments/assets/eebc4bab-9443-4dc7-bb03-bbf969a59b6c" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
