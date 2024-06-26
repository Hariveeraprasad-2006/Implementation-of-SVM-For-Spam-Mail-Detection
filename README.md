# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages.

2.Read the given csv file and display the few contents of the data.Assign the features for x and y respectively.

3.Split the x and y sets into train and test sets.Convert the Alphabetical data to numeric using CountVectorizer.

4.Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.

5.Find the accuracy of the model.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Arikatla Hari Veera Prasad
RegisterNumber:  212223240014
import chardet
file = '/content/spam.csv'
with open(file,'rb') as rawdata:
  result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data= pd.read_csv("/content/spam.csv",encoding='Windows-1252')

data.head()

data.info()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()

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
*/
```

## Output:
## HEAD():
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145049988/8c099d03-6414-4a14-8556-37877be9a1ef)
## INFO():
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145049988/e998dbf7-8bb8-4d9a-93c6-acdcaac1b72d)
## ISNULL().SUM():
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145049988/c5250850-832e-4085-ba97-5f231f05c3ec)
## PREDICTED VALUE:
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145049988/c69eae0a-009f-4c09-9a9b-11dfa0e19050)
## ACCURACY:
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145049988/4ac94c1c-e65c-477a-8bef-9462da9efd89)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
