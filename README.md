# Ex.No.1---Data-Preprocessing
## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## REQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

Kaggle :
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

Data Preprocessing:

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

Need of Data Preprocessing :

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
```
1.Importing the libraries
2.Importing the dataset
3.Taking care of missing data
4.Encoding categorical data
5.Normalizing the data
6.Splitting the data into test and train
```
## PROGRAM:
```
Register Number: 212221220009
Name: Dharshini S
import pandas as pd
df=pd.read_csv("/content/Churn_Modelling.csv")
df.head()
df.isnull().sum()
df.drop(["RowNumber","Age","Gender","Geography","Surname"],inplace=True,axis=1)
print(df)
x=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(x)
print(y)
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
df1 = pd.DataFrame(scaler.fit_transform(df))
print(df1)
from sklearn.model_selection import train_test_split
xtrain,ytrain,xtest,ytest=train_test_split(x,y,test_size=0.2,random_state=2)
print(xtrain)
print(len(xtrain))
print(xtest)
print(len(xtest))
from sklearn.preprocessing import StandardScaler
sc = StandardScaler()
df1 = sc.fit_transform(df)
print(df1)
```
## OUTPUT:
## Dataset:
![Screenshot (11)](https://user-images.githubusercontent.com/113699377/190868267-315176bb-763d-46b7-808b-6cb1d3c4e097.png)
## Discribing data:
![Screenshot (12)](https://user-images.githubusercontent.com/113699377/190868281-cdb7d420-4d6a-4511-b38a-30cb2b027bf0.png)
## Normalized data:
![Screenshot (13)](https://user-images.githubusercontent.com/113699377/190868329-a82a22f5-304f-4ef0-9d7f-deb2ff283ff7.png)
## X_train and Y_train values:
![Screenshot (14)](https://user-images.githubusercontent.com/113699377/190868390-9f0904a8-792f-4605-a41a-5f70434d3726.png)
## X and Y values:
![Screenshot (15)](https://user-images.githubusercontent.com/113699377/190868428-ec697685-ce41-43dc-86b0-693d6e8b8e21.png)
## X_test and Y_test values:
![Screenshot (16)](https://user-images.githubusercontent.com/113699377/190868454-d5e8ba89-62d7-49a9-9e00-67890302112a.png)


## RESULT
Thus the above program for standardizing the given data was implemented successfully
