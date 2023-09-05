# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
Name : VIJIS DURAI R
Register Number : 212222220057
```
*Data Cleaning - Data_set.csv*
import pandas as pd 
df = pd.read_csv("/content/Data_set.csv")
import numpy as np
import pandas as pd
import seaborn as sbn
df = pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on'] = df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network'] = df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] =df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers'] = df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
## OUPUT
OUTPUT FOR DATA 1
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/3a909775-b844-4a2a-a196-aff293f96493)
## Before cleaning
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/3f8c93d0-1c7a-4336-947f-16874c85d277)
## Mode
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/e1a2b180-6f33-44dc-a383-88a8747e2978)
## Mean
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/d5c14bc2-7cda-4893-b0d5-1dbecb8d334c)
## Median
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/25120bbc-60f5-4e57-8817-8c0280374318)
## After Cleaning
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/d34317b8-1c77-4d75-bca7-db6246bf4894)

#CODE FOR DATA 2
Name : VIJIS DURAI R
Register Number : 212222220057
```
import pandas as pd
import numpy as np
import seaborn as sns
from google.colab import files
uploaded = files.upload()
df = pd.read_csv("Loan_data.csv")
df
df.head(5)
df.describe()
df.info()
df.tail()
df.isnull()
df.isnull().sum()
df.shape
df.columns
df.duplicated()
df['Gender'] = df["Gender"].fillna(df['Gender'].mode()[0])
df['Married'] = df["Married"].fillna(df['Married'].mode()[0])
df['Self_Employed'] = df["Self_Employed"].fillna(df['Self_Employed'].mode()[0])
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].mean())
df['Loan_Amount_Term'] = df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['Credit_History'] = df['Credit_History'].fillna(df['Credit_History'].mean())
sns.boxplot(y="LoanAmount",data=df)
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].median())
df.head()
df.isnull().sum()
df.info()
```
# OUTPUT FOR DATA 2
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/e6924869-f862-4541-bfdb-fd9d25a296df)
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/7705af73-5c45-4826-9059-5c844e131b18)
## BEFORE CLEANING
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/c8a807c0-32de-4d34-987d-3850688d98ff)
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/34bdcd7f-1b73-4584-b23f-6e02bff4c51b)
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/b0fc603c-f258-468d-a332-3d0a2787b55f)
## MODE
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/151360a5-7bcb-474c-8ed0-40963bb6fa10)
## MEAN
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/53ba60e5-c76a-4f95-84ab-e007e2387296)
## MEDIAN
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/b5cf48bb-ff20-4aff-aa8e-26ae0484f5c1)
## AFTER CLEANING
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex01/assets/118343184/8dae87bf-2287-467d-beed-49854ccb8daa)
## RESULT
Thus the given data is read,cleansed and cleaned data is saved into the file.
