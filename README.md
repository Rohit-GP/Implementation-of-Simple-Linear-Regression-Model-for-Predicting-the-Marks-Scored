# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored
## AIM:
To implement a simple Linear Regression Model for predicting the marks scored.

## Equipments Required:
Hardware – PCs

Software - Google Colab

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
import pandas as pd
import matplotlib.pyplot as plt

df=pd.read_csv('/content/student_scores.csv')
x=df['Hours'].values
y=df['Scores'].values

x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
denom=0

for i in range(len(x)):
  num+=(x[i]-x_mean)*(y[i]-y_mean)
  denom+=(x[i]-x_mean)**2

m=num/denom

b = y_mean - m * x_mean

print('Slope: ',m)
print('Y-intercept: ',b)

y_predicted=m*x+b #y = mx + c
print('Predicted values: ',y_predicted)

plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.title('LINEAR REGRESSION GRAPH')
plt.xlabel('Hours Studied')    
plt.ylabel('Scores Obtained')  
plt.show()
```

## Output:

![Screenshot 2025-04-17 091230](https://github.com/user-attachments/assets/5ec579d2-6557-4b30-b9d8-f99d6d71c603)

## Result:
Thus the Simple Linear Regression was implemented for predicting the marks scored using python programming.
