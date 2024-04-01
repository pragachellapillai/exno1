# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv") 
df 
```
![Screenshot 2024-04-01 093531](https://github.com/pragachellapillai/exno1/assets/148254952/c2118c47-1404-47fa-bca8-7efc04799441)
```
df.shape
```
![Screenshot 2024-04-01 093857](https://github.com/pragachellapillai/exno1/assets/148254952/2a4b8ce3-1198-443d-9cfb-53352ff29fbf)
```
df.describe()
```
![Screenshot 2024-04-01 093951](https://github.com/pragachellapillai/exno1/assets/148254952/48c3db1e-ea65-429b-8683-e2883e6bcfd1)
```
df.info()
```
![Screenshot 2024-04-01 094055](https://github.com/pragachellapillai/exno1/assets/148254952/7a633a2c-9f37-4f70-9afe-ff56063166ba)
```
df.isnull().sum()
```
![Screenshot 2024-04-01 094223](https://github.com/pragachellapillai/exno1/assets/148254952/eee3f349-8394-4c29-a4a3-0f5e42e0e02e)
```
df.nunique()
```
![Screenshot 2024-04-01 094238](https://github.com/pragachellapillai/exno1/assets/148254952/ef688bcc-1d36-48b4-8ce0-507ecb56282a)
```
df['GENDER'].value_counts()
```
![Screenshot 2024-04-01 094452](https://github.com/pragachellapillai/exno1/assets/148254952/c311b7b1-446c-4580-82f0-99828eee0169)
```
x=df.dropna(how='any')
x
```
![Screenshot 2024-04-01 094502](https://github.com/pragachellapillai/exno1/assets/148254952/ece797b5-371b-4172-935e-9ad54795e919)
```
X2=df.dropna(how='all').shape
df
```

![Screenshot 2024-04-01 094516](https://github.com/pragachellapillai/exno1/assets/148254952/e24dff8f-a765-4e6d-ae0f-f08b4c9689e2)
```
df.dropna(subset=['TOTAL'],how='any').shape
```
![Screenshot 2024-04-01 094933](https://github.com/pragachellapillai/exno1/assets/148254952/e77104ad-3690-4fdf-881a-76e60053b0f3)

```
tot=df.dropna(subset=['M1','M2','M3','M4'],how='any')
tot
```

![Screenshot 2024-04-01 094942](https://github.com/pragachellapillai/exno1/assets/148254952/cf3c1019-d76e-442d-8c11-b0a7a30ef110)

```
df.fillna(0)
```

![Screenshot 2024-04-01 094951](https://github.com/pragachellapillai/exno1/assets/148254952/e3a405ee-1611-4183-a982-6674e9630a65)

# Result
          <<include your Result here>>
