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


# OUTPUT FOR DATA 1


![1](https://user-images.githubusercontent.com/93901857/189408463-6dcb0f99-88df-4c2a-b6f5-483290965dd8.jpeg)
![2](https://user-images.githubusercontent.com/93901857/189408471-bf11a70d-d813-4f69-99c1-06f8ce16bbd8.jpeg)
![3](https://user-images.githubusercontent.com/93901857/189408474-cde337ed-86b8-4fb1-a6bc-486cb669512a.jpeg)
![4](https://user-images.githubusercontent.com/93901857/189408475-fd798d66-67e4-4ef4-9240-1b31a8d88036.jpeg)
![5](https://user-images.githubusercontent.com/93901857/189408479-86dec374-4db9-4d14-a434-719f85177f13.jpeg)
![6](https://user-images.githubusercontent.com/93901857/189408484-e4774740-45c8-46c5-90b5-cfe59edbe0a6.jpeg)
![7](https://user-images.githubusercontent.com/93901857/189408490-8f723f4f-e462-41d9-b82f-a8b72a60c2bc.jpeg)
![8](https://user-images.githubusercontent.com/93901857/189408492-8062bccd-bf60-484b-a1f5-dd695af2d635.jpeg)
![9](https://user-images.githubusercontent.com/93901857/189408495-f8f22dff-0614-4a06-862f-7e25225b3e8f.jpeg)
![10](https://user-images.githubusercontent.com/93901857/189408496-518226c3-1fdc-44a5-a62a-396c02102531.jpeg)

![11](https://user-images.githubusercontent.com/93901857/189410758-98b22481-1507-4380-890d-b6b4ec18c637.jpeg)
![12](https://user-images.githubusercontent.com/93901857/189410762-93716ce7-1f0c-4dd3-b980-f35ee3784c08.jpeg)
![13](https://user-images.githubusercontent.com/93901857/189410764-2ca3ed1d-8085-46ea-8229-92d00db55738.jpeg)


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


![2-1](https://user-images.githubusercontent.com/93901857/189519384-d362b0bb-3e29-47b4-9e03-29ce51d24f7c.jpeg)
![2-2](https://user-images.githubusercontent.com/93901857/189519387-8e2e03f3-3744-4f9a-b04c-a33d647eae4f.jpeg)
![2-3](https://user-images.githubusercontent.com/93901857/189519389-b0f7a67d-3ae2-4735-8da3-95839041fc16.jpeg)
![2-4](https://user-images.githubusercontent.com/93901857/189519391-8d42ad95-909e-4dc8-8a11-5b6ea6965bab.jpeg)
![2-5](https://user-images.githubusercontent.com/93901857/189519399-42c9540f-31d6-4748-8f4b-5bbb74719959.jpeg)
![2-6](https://user-images.githubusercontent.com/93901857/189519403-5b58b5a5-953e-4ebf-865b-039929d92a03.jpeg)
![2-7](https://user-images.githubusercontent.com/93901857/189519404-328f0ab6-2ee8-4bde-8fc1-c0a0a856a030.jpeg)

# Result
The given data is read and data cleaning is performed and the cleaned data is saved to a file
