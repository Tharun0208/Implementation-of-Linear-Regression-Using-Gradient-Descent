# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries, NumPy and Matplotlib.
2. Initialize the population and profit data for different cities.
3. Calculate the slope and intercept using Gradient Descent by updating the parameters to minimize the prediction error.
4. Predict the profit, display the results, and plot the data with the regression line.

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: THARUN R
RegisterNumber:  212224240172
*/
```python
import numpy as np
import matplotlib.pyplot as plt

# Input data: Population of cities and their profits
X = np.array([1, 2, 3, 4, 5], dtype=float)
Y = np.array([2, 4, 5, 4, 5], dtype=float)

# Initialize parameters
m = 0.0
b = 0.0
learning_rate = 0.01
iterations = 1000
n = len(X)

# Gradient Descent
for i in range(iterations):
    Y_pred = m * X + b

    dm = (-2 / n) * np.sum(X * (Y - Y_pred))
    db = (-2 / n) * np.sum(Y - Y_pred)

    m = m - learning_rate * dm
    b = b - learning_rate * db

# Predict profit for a population of 6
population = 6
predicted_profit = m * population + b

print("Slope (m):", round(m, 2))
print("Intercept (b):", round(b, 2))
print("Predicted profit for population 6:", round(predicted_profit, 2))

# Plot the graph
plt.scatter(X, Y, label="Actual Data")
plt.plot(X, m * X + b, label="Regression Line")
plt.xlabel("Population")
plt.ylabel("Profit")
plt.title("Linear Regression Using Gradient Descent")
plt.legend()
plt.show()
```


## Output:

<img width="812" height="662" alt="image" src="https://github.com/user-attachments/assets/3b0a0b0e-5aae-4a3d-9ebe-9c8a6aba1452" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
