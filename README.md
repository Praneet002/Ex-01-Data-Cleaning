#Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE FOR DATA 1

```
'''
Program developed by: PRANEET.S
Register number: 212221230078

'''
import pandas as pd
import numpy as np
import seaborn as sns
df = pd.read_csv("Data_set.csv")
df
df.head()
df.describe()
df.info()
df.tail()
df.shape
df.columns
df.isnull().sum()
df.duplicated()
#Using mode method to fill the data in columns as Object(String)
#mode()[0] - Takes the most reccuring value and fills the empty cells
df['show_name'] = df['show_name'].fillna(df['show_name'].mode()[0])
df['aired_on'] = df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network'] = df['original_network'].fillna(df['original_network'].mode()[0])

sns.boxplot(x="rating",data=df)

#Using mean method to fill the data
df['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df['watchers'] = df['watchers'].fillna(df['watchers'].mean())

#Checking the total no.of null values again
df.isnull().sum()

#Checking info of the dataset to check all the columns have entries
df.info()
```

# OUTPUT FOR DATA 1


![1](https://user-images.githubusercontent.com/94308200/189953869-5f8c5458-848f-4cb9-902e-4b5252f554f7.jpeg)
![2](https://user-images.githubusercontent.com/94308200/189953879-27470009-36fc-4d71-bf6e-3c6b1532f85a.jpeg)
![3](https://user-images.githubusercontent.com/94308200/189953921-dca506b1-61b7-43e5-b9ba-8b7e6cf5dda6.jpeg)
![4](https://user-images.githubusercontent.com/94308200/189953923-935a86c7-b94d-4055-a613-984b7b9bcf8d.jpeg)
![5](https://user-images.githubusercontent.com/94308200/189953930-ca8865f3-9bf8-4f3a-b67c-346fd9a325c3.jpeg)
![6](https://user-images.githubusercontent.com/94308200/189953934-7641ae7a-3e67-42be-a64c-a601437843c2.jpeg)
![7](https://user-images.githubusercontent.com/94308200/189953936-74d03807-a893-4afb-8da9-19b9f653a870.jpeg)
![8](https://user-images.githubusercontent.com/94308200/189953943-abb3c403-94c4-4896-934f-f6677bd58d40.jpeg)
![9](https://user-images.githubusercontent.com/94308200/189953947-83ecf23b-85e6-4bab-8e68-8568a0c8a303.jpeg)
![10](https://user-images.githubusercontent.com/94308200/189953949-904ee43c-c4e6-4d63-95b6-ac5874762b6d.jpeg)
![11](https://user-images.githubusercontent.com/94308200/189953958-7b297755-48d1-4f67-8a8b-56b6821fbf4e.jpeg)
![12](https://user-images.githubusercontent.com/94308200/189953965-52a01ac8-4dfe-4d75-b70a-e626e0b4372c.jpeg)
![13](https://user-images.githubusercontent.com/94308200/189953971-6be3e64e-936b-4ec4-b094-cfca1bc10af2.jpeg)



# CODE FOR DATA 2

```
'''
Program developed by: PRANEET.S
Register number: 212221230078
'''
import pandas as pd
import numpy as np
import seaborn as sns
d = pd.read_csv("/content/Loan_data.csv")
d
d.head()
d.describe()
d.tail()
d.isnull().sum()
d.shape
d.columns
d.duplicated

#Using mode method to fill the data in columns as Object(String)
#mode()[0] - Takes the most reccuring value and fills the empty cells
d['Gender'] = d['Gender'].fillna(d['Gender'].mode()[0])
d['Dependents'] = d['Dependents'].fillna(d['Dependents'].mode()[0])
d['Self_Employed'] = d['Self_Employed'].fillna(d['Self_Employed'].mode()[0])

#Using mean method to fill the data
d['LoanAmount'] = d['LoanAmount'].fillna(d['LoanAmount'].mean())
d['Loan_Amount_Term'] = d['Loan_Amount_Term'].fillna(d['Loan_Amount_Term'].mean())
d['Credit_History'] = d['Credit_History'].fillna(d['Credit_History'].mean())

sns.boxplot(y="LoanAmount",data=d)

#Checking the total no.of null values
again
d.isnull().sum()

#Checking info of the dataset to check all the columns have entries
d.info()

```

# OUTPUT FOR DATA 2


![2-1](https://user-images.githubusercontent.com/94308200/189953884-f0ec6f3a-d75f-4497-bbf1-78e72db3b15c.jpeg)
![2-2](https://user-images.githubusercontent.com/94308200/189953888-dbe2dbe0-d28f-4e5d-a85f-63706c18e242.jpeg)
![2-3](https://user-images.githubusercontent.com/94308200/189953895-9f0dc82e-ceda-49e8-ab26-9ea100f087d1.jpeg)
![2-4](https://user-images.githubusercontent.com/94308200/189953901-a02271db-9e9c-4ac8-947d-2ffe40bf4be1.jpeg)
![2-5](https://user-images.githubusercontent.com/94308200/189953904-6e8a51bc-f1af-45da-95c7-4a6acf0a6f17.jpeg)
![2-6](https://user-images.githubusercontent.com/94308200/189953910-a6e0fafb-ec77-4dd9-b28a-fa33d12f13ac.jpeg)
![2-7](https://user-images.githubusercontent.com/94308200/189953915-f81fc230-be90-4fe6-b9b2-0545ce8add5b.jpeg)

# Result
The given data is read and data cleaning is performed and the cleaned data is saved to a file
