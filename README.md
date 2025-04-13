# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored
## AIM:
To implement a simple Linear Regression Model for predicting the marks scored.

## Equipments Required:
Hardware – PCs

Anaconda – Google Colab

## Algorithm
1. Get the independent variable X(hours studied) and dependent variable Y(marks scored).
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.
4. Compute the y -intercept of the line by using the formula:
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.
  
## Program:

Program to implement univariate Linear Regression to fit a straight line using least squares.

Developed by: Rohit GP

RegisterNumber: 24900185

```
import numpy as np
import matplotlib.pyplot as plt

x=np.array(eval(input()))
y=np.array(eval(input()))

x_mean=np.mean(x)
y_mean=np.mean(y)
n,d=0,0

for i in range(1,len(x)+1):
    n+=(x[i-1]-x_mean)*(y[i-1]-y_mean)
    d+=(x[i-1]-x_mean)**2

m=n/d
b=y_mean-(m*x_mean)
y_pred=m*x+b
print(y_pred)
2
plt.scatter(x,y)
plt.plot(x,y_pred,color='red')
plt.xlabel('Hours Studied')
plt.ylabel('Marks Scored')
plt.title('Linear Reggression Graph')
plt.show()
```

## Output:

![Screenshot 2025-04-13 122440](https://github.com/user-attachments/assets/f6163f6a-4e46-4235-8c1a-9a799bf00bf1)

## Result:
Thus the Simple Linear Regression was implemented for predicting the marks scored using python programming.
