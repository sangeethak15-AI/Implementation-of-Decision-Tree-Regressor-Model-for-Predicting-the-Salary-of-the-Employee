# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Sangeetha.K
RegisterNumber: 212221230085 
*/
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![ml71](https://user-images.githubusercontent.com/93992063/200124715-135f54e6-330e-4497-963d-96600cd67f75.png)


![ml77](https://user-images.githubusercontent.com/93992063/200124819-07ec341f-3ca9-45e7-9efe-2558c17e5a3e.png)

![ml78](https://user-images.githubusercontent.com/93992063/200124829-33473f25-31d4-4729-afbd-2866a0765136.png)

![ml79](https://user-images.githubusercontent.com/93992063/200124732-d2d0fd47-39fe-4ea9-ac89-2336d75c2a56.png)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
