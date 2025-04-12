# Implementation of Univariate Linear Regression
# Developed by: Siddharth S
# RegisterNumber: 212224040317 

## AIM: To implement univariate Linear Regression to fit a straight line using least squares.


## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
#Program to implement univariate Linear Regression to fit a straight line using least squares.


import numpy as np
import matplotlib.pyplot as plt

# Input values as lists, e.g., [1, 2, 3, 4]
X = np.array(eval(input("Enter X values as a list: ")))
Y = np.array(eval(input("Enter Y values as a list: ")))

# Calculate means
x_mean = np.mean(X)
y_mean = np.mean(Y)

# Initialize numerator and denominator
num = 0
demo = 0

# Calculate slope (m)
for i in range(len(X)):
    num += (X[i] - x_mean) * (Y[i] - y_mean)
    demo += (X[i] - x_mean) ** 2

m = num / demo

# Calculate intercept (b)
b = y_mean - m * x_mean

# Predict Y values
y_pred = m * X + b

# Output results
print("Slope:", m)
print("Intercept:", b)
print("Predicted values:", y_pred)

# Plotting
plt.scatter(X, Y, label="Original Data")
plt.plot(X, y_pred, color="red", label="Regression Line")
plt.title("Linear Regression Graph")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.show()


*/
```

## Output:

![alt text](<Screenshot 2025-04-11 232352.png>)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
