<img width="793" height="567" alt="image" src="https://github.com/user-attachments/assets/233e09c4-8899-4875-bb5d-328171425d03" /># Implementation of Univariate Linear Regression
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
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
xmean=np.mean(X)
ymean=np.mean(Y)
num,den=0,0
for i in range(len(X)):
  num+=(X[i]-xmean)*(Y[i]-ymean)
  den+=(X[i]-xmean)**2
slope=num/den
c=ymean-slope*xmean
y_pred=slope*X+c
plt.scatter(X,Y,color="blue")
plt.plot(X,y_pred,"red")
plt.show()






```
## Output
<img width="793" height="567" alt="Screenshot 2025-10-30 115452" src="https://github.com/user-attachments/assets/4c53c0a4-af53-4029-b0e6-9c5ff7d418d1" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
