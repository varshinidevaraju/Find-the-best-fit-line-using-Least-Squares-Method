# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.
   
![image](https://github.com/user-attachments/assets/4ec85932-e081-4da8-b59d-6bfdd329fa61)

4. Compute the y -intercept of the line by using the formula:
   
![image](https://github.com/user-attachments/assets/dc6c7f0e-6956-442a-ae35-c8237f1069c8)

5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program:

```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: D.Varshini
RegisterNumber:212223230234

import numpy as np
import matplotlib.pyplot as plt

x=np.array(eval(input("Enter the value:")))
y=np.array(eval(input("Enter the value:")))
x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
denom=0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2

m=num/denom

b=y_mean-m*x_mean
print("Name: Sukirthana.M\n Reg.no: 212224220112")
print("Slope{}\nY.intercept{}:".format(m,b))

y_predicted=m*x+b
print(y_predicted)
      
plt.scatter(x,y)
plt.plot(x,y_predicted, color='red')
plt.show()
```


## Output:

![ml1](https://github.com/user-attachments/assets/f4a7b6a4-f8eb-4729-bc64-ff566fb40ae9)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
