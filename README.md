# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to implement the simple linear regression model for predicting the marks scored.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the program
2. Import the numpy,pandas,matplotlib
3. Read the dataset of student scores
4. Assign the columns  hours to x and columns scores to y
5. From sklearn library select the model to train and test the dataset
6. Plot the training set and testing set in the graph using matplotlib library
7. Stop the program

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Beauty Kumari S
RegisterNumber:  212220040023
*/
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
dataset=pd.read_csv("/content/student_scores .csv")
dataset.head() #printing top 5 rows
X=dataset.iloc[:,:-1].values #assigning colum hours to X
Y=dataset.iloc[:,1].values   #assigning colum scores to Y
print(X)
print(Y)
from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test=train_test_split(X,Y,test_size=1/3,random_state=0)
from sklearn.linear_model import LinearRegression
regressor=LinearRegression()
regressor.fit(X_train,Y_train)
Y_pred=regressor.predict(X_test)
plt.scatter(X_train,Y_train,color='red')
plt.plot(X_train,regressor.predict(X_train),color='Black')
plt.title("hr vs sec(Training set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()
plt.scatter(X_test,Y_test,color='Green')
plt.plot(X_test,regressor.predict(X_test),color='Blue')
plt.title("hr vs sec(Training set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()
```

## Output:
![simple linear regression model for predicting the marks scored](./images/op3.jpeg)
![simple linear regression model for predicting the marks scored](./images/op4.jpeg)

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
