# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. mport the required packages.

2.Import the dataset to operate on.

3.Split the dataset.

4.Predict the required output.

5.End the program. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: v.sreeja
RegisterNumber:  212222230169
*/
import pandas as pd
data=pd.read_csv('/content/spam.csv',encoding='Windows-1252')

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

```
## Output:

![Screenshot (281)](https://github.com/VelasiriSreeja/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118344328/3bf9555b-014a-4489-af50-13a16e45ebe3)

![Screenshot (282)](https://github.com/VelasiriSreeja/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118344328/9cc04007-ad10-462b-9433-d0f0360ac245)


![Screenshot (283)](https://github.com/VelasiriSreeja/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118344328/3566166c-bf66-405c-aac8-84245e7c904f)

![Screenshot (285)](https://github.com/VelasiriSreeja/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118344328/85d87316-fc44-4633-8231-5aeae26457e1)


![Screenshot (284)](https://github.com/VelasiriSreeja/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118344328/19927bc2-5139-4769-947d-331d20509829)


![Screenshot (286)](https://github.com/VelasiriSreeja/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118344328/a5c51faa-50e7-4440-97d4-99aca435a155)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
