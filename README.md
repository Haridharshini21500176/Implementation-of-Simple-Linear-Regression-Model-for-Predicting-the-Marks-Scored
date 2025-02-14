# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the needed packages

2.Assigning hours To X and Scores to Y

3.Plot the scatter plot

4.Use mse,rmse,mae formmula to find

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: S.Haridharshini
RegisterNumber: 212221230033 
*/
```
```

#import files
import numpy as np
import pandas as pd
df=pd.read_csv('student_scores.csv')

assigning hours To X and Scores to Y

X=df.iloc[:,:-1].values
Y=df.iloc[:,1].values
print("X=",X)
print("Y=",Y)

from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test=train_test_split(X,Y,test_size=1/3,random_state=0)

from sklearn.linear_model import LinearRegression
reg=LinearRegression()
reg.fit(X_train,Y_train)

Y_pred=reg.predict(X_test)
import matplotlib.pyplot as plt
from sklearn.metrics import mean_absolute_error,mean_squared_error

plt.scatter(X_train,Y_train,color='brown')
plt.plot(X_train,reg.predict(X_train),color='orange')
plt.title('Training set(H vs S)',color='green')
plt.xlabel('Hours',color='pink')
plt.ylabel('Scores',color='pink')

plt.scatter(X_test,Y_test,color='brown')
plt.plot(X_test,reg.predict(X_test),color='violet')
plt.title('Test set(H vs S)',color='brown')
plt.xlabel('Hours',color='grey')
plt.ylabel('Scores',color='grey')

mse=mean_squared_error(Y_test,Y_pred)
print('MSE = ',mse)

mae=mean_absolute_error(Y_test,Y_pred)
print('MAE = ',mae)

rmse=np.sqrt(mse)
print('RMSE = ',rmse)

```


## Output:
![mx1](https://user-images.githubusercontent.com/94168395/204467046-1e1bf69b-244d-469c-ae85-18c7fd8d1dd7.png)

![30a](https://user-images.githubusercontent.com/94168395/204467126-a00d6531-f4d7-432a-b690-fe2ac805d55d.png)

![30b](https://user-images.githubusercontent.com/94168395/204467148-f02b2a81-3068-4db4-be85-d8022c7de51f.png)

![193458177-655b6c90-ddb6-43ce-b9af-dd11ca45c20a](https://user-images.githubusercontent.com/94169318/193607735-68f645dc-8340-49c2-b22e-74e104856d1a.png)

![193458190-589570af-b80c-4577-a0e4-84ba844e85f8](https://user-images.githubusercontent.com/94169318/193607779-61905f2d-ed8c-4ba5-b105-f096c9f1f616.png)

![193458190-589570af-b80c-4577-a0e4-84ba844e85f8](https://user-images.githubusercontent.com/94169318/193608043-0a8987a5-d757-4099-9410-0bc854bd54fa.png)

![193458198-ed30b519-f24d-4ca8-ae33-5374ced8a49f](https://user-images.githubusercontent.com/94169318/193608117-0ea88216-e9e4-41e8-bc79-a6ff1470491d.png)

![204101850-736e9c41-d29c-49d8-a7c1-da65ab29905a](https://user-images.githubusercontent.com/94168395/204488982-f3f98580-0281-4d33-a28f-7246b5439838.jpg)

![204101843-3782c792-a6a5-457a-8f22-c23827a7c79d](https://user-images.githubusercontent.com/94168395/204488842-1962afba-791e-4916-a2b6-d26032f78427.jpg)

![193458202-cfa670e3-f16a-4a11-920d-c832f943f069](https://user-images.githubusercontent.com/94169318/193608163-e9e7f42d-8ceb-4428-8081-e577100a660d.png)



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
