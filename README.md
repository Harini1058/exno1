<img width="1920" height="1080" alt="{DE3E6C75-3EF0-4610-B83A-BF81927BB56C}" src="https://github.com/user-attachments/assets/242aba19-0444-4f53-87d3-c7efd1ef2c51" /># Exno:1
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
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
print(df)
df.info()
<img width="1920" height="1080" alt="Screenshot 2025-10-04 084316" src="https://github.com/user-attachments/assets/647de584-3706-4831-a83e-efcf8a2f50e4" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
dff=df.isnull().sum()
print (dff)

<img width="1920" height="1080" alt="Screenshot 2025-10-04 084527" src="https://github.com/user-attachments/assets/756765be-101e-43b6-b585-9efc050a2e5b" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
dfd=df.dropna(axis=1)
print (df)
print ("after dropna")
print (dfd)
df.info()

<img width="723" height="840" alt="Screenshot 2025-10-04 084659" src="https://github.com/user-attachments/assets/146e90c6-95f1-41ee-b66c-f9c0b35d1607" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
dfd=df.dropna(axis=1,inplace=True)
print (df)
print ("after dropna")
print (dfd)

<img width="907" height="474" alt="Screenshot 2025-10-04 084910" src="https://github.com/user-attachments/assets/b072e3b3-9341-4e8d-be30-b1b7463fc10c" />


import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
dfd=df.dropna(axis=1)
print (df)
print ("after dropna")
print (dfd)
df.info()

<img width="578" height="838" alt="Screenshot 2025-10-04 085017" src="https://github.com/user-attachments/assets/ccd15a17-b2d5-4681-9fa3-5bc8fdadc223" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
dfd=df.dropna(axis=1)
print (df)
print ("after dropna")
print (dfd)
df.filter(regex='e|a', axis=1)


<img width="683" height="829" alt="Screenshot 2025-10-04 085436" src="https://github.com/user-attachments/assets/4340175d-60a1-4a8c-8cc2-1d5195c664d1" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
dfd=df.dropna(axis=1)
print (df)
print ("after dropna")
print (dfd)
filtered_df=df.filter(regex='e$',axis=1)
print(filtered_df)

<img width="820" height="884" alt="Screenshot 2025-10-04 085536" src="https://github.com/user-attachments/assets/2e9eaf78-2e04-4cbf-bd08-7c5ebf9e4ed1" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
dfd=df.dropna(axis=1)
print (df)
print ("after dropna")
print (dfd) 
df.iloc[0:4,1:4]

<img width="712" height="899" alt="Screenshot 2025-10-04 085706" src="https://github.com/user-attachments/assets/720fe3b5-2cd7-436f-b75d-f17ed41501ca" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
dfd=df.fillna
print (df)
print ("after fillna")
print (dfd) 

<img width="748" height="848" alt="Screenshot 2025-10-04 085940" src="https://github.com/user-attachments/assets/9be0a245-93cc-4638-a8e6-0ad454cb4997" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
print (df)
df.fillna(method='ffill')

<img width="835" height="922" alt="Screenshot 2025-10-04 090218" src="https://github.com/user-attachments/assets/a19e2114-78d8-4439-a198-9ee7f066663f" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
print (df)
df.fillna(method="bfill")

<img width="762" height="848" alt="Screenshot 2025-10-04 090412" src="https://github.com/user-attachments/assets/14cb66b1-48e5-4cea-9586-5457c180bc7b" />

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
data=pd.read_csv("iris.csv")
df=pd.DataFrame(data)
print (df)   
df.info()

<img width="790" height="519" alt="Screenshot 2025-10-04 090743" src="https://github.com/user-attachments/assets/49d07df9-4419-4044-a660-5b3922a530cb" />

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
data=pd.read_csv("iris.csv")
df=pd.DataFrame(data)
print (df)   
df.describe()

<img width="719" height="578" alt="Screenshot 2025-10-04 090824" src="https://github.com/user-attachments/assets/f6faa38d-4d45-449c-94ff-5842229866b0" />

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
data=pd.read_csv("iris.csv")
df=pd.DataFrame(data)
print (df)    
x=df["species"]
y=df["sepal_length"]
plt.xlabel('X-axis')
plt.ylabel('Y-axis') 
plt.plot(x,y)
plt.show()

<img width="913" height="910" alt="Screenshot 2025-10-04 091158" src="https://github.com/user-attachments/assets/8a4d0769-ba5d-46d7-aa27-579f8aeceea4" />

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
data=pd.read_csv("iris.csv")
df=pd.DataFrame(data)
print (df)    
x=df["species"]
y=df["sepal_length"]
plt.bar(x,y)
plt.show()

<img width="824" height="889" alt="Screenshot 2025-10-04 091325" src="https://github.com/user-attachments/assets/4cac5bb6-ba93-4d8c-8e88-3c76f220725f" />

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
data=pd.read_csv("iris.csv")
df=pd.DataFrame(data)
print (df)    
x=df["petal_width"]
y=df["sepal_length"]
plt.plot(x,y,)
plt.show()

<img width="1920" height="1080" alt="Screenshot 2025-10-04 091458" src="https://github.com/user-attachments/assets/46bebcb0-5556-401b-85fe-2faf0e08b62f" />

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
data=pd.read_csv("iris.csv")
df=pd.DataFrame(data)
print (df)    
x=df["species"]
y=df["sepal_length"]
plt.plot(x,y,color="purple")
plt.show()

<img width="1920" height="1080" alt="Screenshot 2025-10-04 091640" src="https://github.com/user-attachments/assets/ec08cbc6-0a51-4333-bf68-ca0c6ad4ca46" />

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
data=pd.read_csv("iris.csv")
df=pd.DataFrame(data)
print (df)    
x=df["species"]
y=df["sepal_length"]
plt.scatter(x,y,)
plt.show()

<img width="1920" height="1080" alt="Screenshot 2025-10-04 091813" src="https://github.com/user-attachments/assets/16b47e6b-d343-430c-9bd5-0dbaa8ca5647" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
df_ffilled=df.fillna(method='bfill')
print (df)
df.interpolate()

<img width="878" height="418" alt="Screenshot 2025-10-04 092219" src="https://github.com/user-attachments/assets/36ae443b-6d52-4d5f-9b17-7fdcfee07d79" />

# Result
Thus we have cleaned the data and removed the outliers by detection using IQR and Z-Score method

