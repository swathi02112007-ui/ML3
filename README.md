# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

Step 1: Start
Step 2: Import Libraries
Import numpy, pandas, and StandardScaler from sklearn.
Step 3: Load Dataset
Read the CSV file using pandas.read_csv().
Read the CSV file using pandas.read_csv().
X → Independent variables (all columns except the last).
y → Dependent variable (last column).
Step 4: Preprocess Data
Standardize the features (X) using StandardScaler to improve convergence.
Add a bias column (column of ones) to X for the intercept term.
Step 5: Initialize Parameters
Set all model parameters θ (theta) to zero.
Choose a learning rate (α) and number of iterations.
Step 6: Hypothesis Function
image
Where:
X is the feature matrix (with bias column).
θ is the parameter vector.
Step 7: Cost Function (Mean Squared Error)
WhatsApp Image 2025-09-13 at 14 37 25_2eab0dec

Step 8: Gradient Descent Update Rule
Repeat for the chosen number of iterations:
image
Step 9: Model Training
1.Run gradient descent loop until parameters converge (or max iterations reached).
2.Final learned values of θ represent the trained model.
Step 10: Prediction
For new input data:
1.Scale the features using the same scaler as training.
2.Add the bias term.
3.Compute:
image
Step 11: Output
Print learned parameters.
Print predicted output for new test data.
Step 12: End

## Program:
```
/*
Program to implement the linear regression using gradient descent.

import numpy as np
import pandas as pd 
import matplotlib.pyplot as plt

data = pd.read_csv("50_Startups.csv")

X = data['R&D Spend'].values
y = data['Profit'].values

X =(X - X.mean())/X.std()

m = 0 
b = 0

learning_rate = 0.001
epochs = 2000
n = len(X)

for i in range(epochs):
    y_pred = m * X + b
    
    dm =(-2/n) * np.sum(X * (y - y_pred))
    db =(-2/n) * np.sum(y - y_pred)
    
    m = m - learning_rate * dm
    b = b - learning_rate  * db
    
print("slope(m):",m)
print("intercept (b):",b)

y_pred = m * X + b

plt.scatter(X,y)
plt.plot(X,y_pred)

plt.xlabel("R&D spend(Normalized)")
plt.ylabel("Profit")
plt.title("Gradient Descent of R&D spend and Profit")

plt.show()

Developed by: Swathi P N
RegisterNumber:  212225230279
*/
```

## Output:

![alt text](ml3.1.png)

![alt text](ml3.2.png)

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
