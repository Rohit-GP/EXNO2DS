# EXNO2DS
# AIM:
To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT

Done by : ROHIT GP - 212224220082 / 24900185


```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

dt=pd.read_csv('/content/titanic_dataset (2).csv')
dt
```
![image](https://github.com/user-attachments/assets/bd44eb7b-b891-47e7-a74d-2e5daf515c21)
```
dt.info()
```
![image](https://github.com/user-attachments/assets/3112210f-898c-4fc0-b79b-d570771c41d6)
```
dt.shape
```
![image](https://github.com/user-attachments/assets/8ae250b9-c96e-437b-92e7-00289c0be047)
```
dt.describe ()
```
![image](https://github.com/user-attachments/assets/9f7b8c08-f506-498e-a005-adc8f7ab9cb7)
```
dt.nunique()
```
![image](https://github.com/user-attachments/assets/90b0ab22-f7c2-46df-8e77-b8e4ab17d145)
```
dt['Survived'].value_counts()
```
![image](https://github.com/user-attachments/assets/653380e2-2a61-4381-81bb-85c2d15f762f)
```
sns.countplot(data=dt,x='Survived',palette=['blue','orange'],hue='Survived')
```
![image](https://github.com/user-attachments/assets/c5e82ab7-52d2-45fc-9896-3a2f97de162a)
```
dt.isnull().sum()
```
![image](https://github.com/user-attachments/assets/e73795f2-a19a-4ad5-a1a2-4800f6c6f029)
```
sns.catplot(data=dt,x='Sex',col='Survived',kind='count',palette=['blue','orange'],aspect=0.6,height=5)
```
![image](https://github.com/user-attachments/assets/6a1c6a11-2c69-4c86-9ab2-5bbe717e279e)
```
sns.catplot(data=dt,kind='count',x='Survived',hue='Sex')
```
![image](https://github.com/user-attachments/assets/6e95aff4-7071-413e-9edd-330fa1d2ae5d)
```
dt.boxplot(column='Age',by='Survived')
```
![image](https://github.com/user-attachments/assets/1069df18-9ffd-451d-a16a-ee0e0850d7bc)
```
sns.scatterplot(x=dt['Age'],y=dt['Fare'])
```
![image](https://github.com/user-attachments/assets/ec67356b-a151-4300-a965-ca1394769fb5)
```
sns.jointplot(x=dt['Age'],y=dt['Fare'])
```
![image](https://github.com/user-attachments/assets/893a33a8-fd9d-4cd0-b230-87cf8949195b)
```
fig, ax1=plt.subplots(figsize=(8,5))
pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Sex',data=dt)
```
![image](https://github.com/user-attachments/assets/53b57c6e-4b2c-493a-a994-a21c4e752386)
```
sns.catplot(data=dt,col='Survived',x='Sex',hue='Pclass',kind='count')
```
![image](https://github.com/user-attachments/assets/95abca8b-022e-4145-a1e1-1d20f863ca6d)
```
sns.pairplot(dt)
```
![image](https://github.com/user-attachments/assets/41e53041-a661-43bd-8ed8-d08c83109297)
![image](https://github.com/user-attachments/assets/e4732939-9cc4-448c-912d-138d6cc79be0)


# RESULT
Successfully performed the Exploratory Data Analysis on the given data set.
