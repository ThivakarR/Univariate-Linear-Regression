# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
'''
Program for Univariate linear regression using the least squares method.
Developed by: R.Thivakar
RegisterNumber: 212222240109
'''
import numpy as np
import matplotlib.pyplot as plt
# Preprocessing Input data
X = np.array(eval(input()))
Y = np.array(eval(input()))
# Building the model
XMean=np.mean(X)
YMean=np.mean(Y)
num,den=0,0
for i in range(len(X)):
  num+=(X[i]-XMean)*(Y[i]-YMean)
  den+=(X[i]-XMean)**2
m=num/den
#y=mx+c
c=YMean-m*XMean
print (m, c)
#Predict the output
Y_Pred=m*X+c
print (Y_Pred)
#plotting graph
plt.scatter(X,Y)
plt.plot(X,Y_Pred,color="red")
plt.show()
```
## Output

![Screenshot 2023-06-11 192302](https://github.com/ThivakarR/Univariate-Linear-Regression/assets/118707074/76caaca8-9ce9-48eb-a55a-b6d7d6e095d7)



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
