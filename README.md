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
import pandas as pd
df=pd.read_csv("data_set.csv")
df

<img><img width="1373" height="449" alt="{EB44950D-FEC2-4DFF-BE51-5D05FE379974}" src="https://github.com/user-attachments/assets/5c18c3b2-0668-43ae-afe9-8125f86af463" />

df.isnull()

<img><img width="1263" height="434" alt="{434F441A-EA7C-4366-9AD9-346DFFC2B9AF}" src="https://github.com/user-attachments/assets/2d4f90b5-43a8-4b45-b152-1eaf8573064f" />

df.notnull()

<img><img width="1036" height="425" alt="{59255F0C-A6BE-4511-B455-9E3593134917}" src="https://github.com/user-attachments/assets/bf609116-cb2a-4500-88a6-eff122566122" />

print(df.dropna(axis=0))

<img><img width="779" height="691" alt="{EE5C66CE-26E1-4494-9001-A2D5B317C762}" src="https://github.com/user-attachments/assets/aaff3e2e-423a-4d02-b97e-3378e80adf80" />

dfs=df[df['num_episodes']>20]

dfs

<img><img width="1089" height="647" alt="{32008EF6-417A-447A-B92A-E782FC0441FD}" src="https://github.com/user-attachments/assets/f8a46f8a-1f88-4904-a20c-530fb8f72b34" />

import pandas as pd
df=pd.read_csv("data_set.csv")
df

<img><img width="1065" height="336" alt="{782FCE73-D65D-46E1-8EC5-F09183B5DEB8}" src="https://github.com/user-attachments/assets/d8c8657a-87db-4963-ad59-6eab35583f7c" />


df.iloc[:4]


<img><img width="998" height="139" alt="{7C2F70E3-0445-4164-A32C-20A0E3C8DDE1}" src="https://github.com/user-attachments/assets/029bdfa1-5a31-4a52-b241-d2e675770cc8" />


df.iloc[[1,3,5],[1,3]]



<img><img width="328" height="110" alt="{B421851C-A7C1-4389-A2C6-D6412F1AEE0E}" src="https://github.com/user-attachments/assets/e852c9d6-c6e8-4343-a096-d514282fdc82" />

df.iloc[0:4,1:4]


<img width="385" height="129" alt="{B8619E2E-AA8D-4101-84B1-45D951E70688}" src="https://github.com/user-attachments/assets/78ff00b1-0da3-47a8-826d-7441c7b39d61" />

dff=df.fillna(0)
dff


<img><img width="997" height="355" alt="{C745A5B3-791F-4DEB-A9DF-1B5F195786F7}" src="https://github.com/user-attachments/assets/287af219-ae9e-4bc7-b049-d5b06b5bcd60" />

df.fillna(method='ffill')


<img><img width="985" height="362" alt="{4F0B1608-E097-4A9C-BB9B-13987981DFBE}" src="https://github.com/user-attachments/assets/f61c0b7d-1642-481c-aeb2-16c89729ac1d" />

df.fillna(method='bfill')


<img><img width="1051" height="345" alt="{8DF15A36-A4A1-4708-ACE5-69DBE9D9F909}" src="https://github.com/user-attachments/assets/ecdd9fd3-1a86-46c8-a0f7-c29eefd6523d" />

df['num_episodes'].fillna(value=df['num_episodes'].mean())


<img><img width="374" height="200" alt="{70A0564F-89B0-46E6-9C30-483643DDC027}" src="https://github.com/user-attachments/assets/ea5782f7-1ad9-4abd-b8fc-1ace78014c6f" />



import matplotlib.pyplot as plt

plt.bar(df["country"],df["num_episodes"])
plt.show()



<img><img width="658" height="415" alt="{632FF91C-E356-4D8D-8A40-69AC08323629}" src="https://github.com/user-attachments/assets/62e03490-a0f3-4757-8b42-c6f2a382f40f" />



plt.plot(df["country"],df["num_episodes"])
plt.show


<img><img width="713" height="409" alt="{682FE084-2B59-4D52-A222-34F4B2579AE9}" src="https://github.com/user-attachments/assets/75d42229-b815-4279-b62b-dba6e6a41dbb" />



plt.scatter(df["country"],df["num_episodes"])
plt.show()


<img><img width="744" height="411" alt="{2AD0ACED-E864-4D2D-BC1A-6B56534A6970}" src="https://github.com/user-attachments/assets/ea534ee2-ab9e-468d-acb4-37759ddc51f4" />





# Result
          <<include your Result here>>
