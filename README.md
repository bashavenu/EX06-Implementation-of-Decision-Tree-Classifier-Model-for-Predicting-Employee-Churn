# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.import the employee churn dataset

2.if the dataset has missing values handel them using techiniques such as mean

3.convert categorical variables into numerical format using techniques such as noe_hot encoding

4.scale features if necessary using standardscaler


## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: BASHA VENU
RegisterNumber:  2305001005

import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv('/content/Employee_EX6.csv')
data = pd.read_csv('/content/Employee_EX6.csv')
data = df.copy()
data
le = LabelEncoder()
data['salary'] = le.fit_transform(data['salary'])
data
X = data.drop(['Departments','left'],axis=1)
Y = data['left']
clf = DecisionTreeClassifier()
clf.fit(X,Y)
plt.figure(figsize=(80,80))
plot_tree(clf, feature_names=X.columns,class_names=['LEFT','"NOT LEFT"'],filled=True,fontsize=14)
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/e87a2a0e-1bdf-4d08-8211-53e637a14a17)

![image](https://github.com/user-attachments/assets/b5057feb-8aa4-4871-b538-75e4274dca51)

![image](https://github.com/user-attachments/assets/3d091852-d773-4421-97b1-db7887160cb1)

![image](https://github.com/user-attachments/assets/f2ba96a7-f5ad-4a49-88ca-4e7a58e0bcef)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
