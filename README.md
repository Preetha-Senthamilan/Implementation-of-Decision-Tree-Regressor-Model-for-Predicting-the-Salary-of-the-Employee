# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the libraries and read the data frame using pandas.
2.Calculate the null values present in the dataset and apply label encoder.
3.Determine test and training data set and apply decison tree regression in dataset.
4.calculate Mean square error,data prediction and r2.  
## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: PREETHA.S
RegisterNumber: 212222230110
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

## data.head()

![Screenshot 2023-10-12 091932](https://github.com/Preetha-Senthamilan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119390282/da57082e-f639-4782-841a-736cdfadd7c6)

## data.info()

![Screenshot 2023-10-12 091946](https://github.com/Preetha-Senthamilan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119390282/c9cd2d38-5408-4669-890f-d3e6593e11da)

## data.head for salary

![Screenshot 2023-10-12 092011](https://github.com/Preetha-Senthamilan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119390282/de2acbf4-bf2d-4a5f-a66e-78eebbd0449e)

## MSE value

![Screenshot 2023-10-12 092601](https://github.com/Preetha-Senthamilan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119390282/c1cc772d-4efd-4a82-bd99-b283f7ceec35)


## r2 value

![Screenshot 2023-10-12 092615](https://github.com/Preetha-Senthamilan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119390282/5f4604b8-1d6e-4d96-93f4-c6ba2195fe35)

## data prediction

![Screenshot 2023-10-12 092644](https://github.com/Preetha-Senthamilan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119390282/75fef0b5-08e8-4896-83a1-4fca90278491)






## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
