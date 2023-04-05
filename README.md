# workshop-Multivariate-analysis

AIM:

write a python code to visualize the given data using bivariant analysis.

ALGORITHM:

step1:
import the csv file using pandas package.

step2:
store the data as dataframe in a variable.

step3:
display the information of data sunch as datatypes,value counts,skewness

step4:
display the data in the barplot,scatter plot and heatmap.

CODE:
```
Developed by: Adhithya Perumal.D
Reg.number  : 212222230007

import pandas as pd
import seaborn as sns
from matplotlib import pyplot as plt
df=pd.read_excel('/content/FlightInformation.xlsx')
df
```
```
df.info()
df.dtypes
df['Airline'].value_counts()
df.describe()
```
```
plt.figure(figsize=(30,10))
sns.scatterplot(x=df['Airline'],y=df['Price'],hue=df['Source'])
```
```
prices=df.loc[:,["Airline","Price"]]
prices=prices.groupby(by=["Airline"]).sum().sort_values(by="Price")
plt.figure(figsize=(30,10))
sns.barplot(x=prices.index,y="Price",data=prices)
plt.xticks(rotation=90)
plt.xlabel=("Airline")
plt.ylabel=("Price")
plt.show()
```
```
df=pd.read_excel('/content/FlightInformation.xlsx')
sns.heatmap(df.corr())
```

OUTPUT:
![WORKS](https://user-images.githubusercontent.com/118707079/230082014-910d6282-d2b8-4319-8727-3837d764ddf9.png)

![WORK2](https://user-images.githubusercontent.com/118707079/230082410-11eed3a2-7553-475b-9b46-dc173d8c9b32.png)

![WORK3](https://user-images.githubusercontent.com/118707079/230082426-403c1ad4-ebcd-4d96-99b1-92313895c2e3.png)

![WORK4](https://user-images.githubusercontent.com/118707079/230082440-9a7576b9-aa7f-42fd-ab1e-65d0176f6fc7.png)

![WORK5](https://user-images.githubusercontent.com/118707079/230082470-f8492001-a47f-4825-844b-41274e447a02.png)

![WORK6](https://user-images.githubusercontent.com/118707079/230082486-ea64e94d-a34a-46a1-8b32-38578e21fcbe.png)

![WORK7](https://user-images.githubusercontent.com/118707079/230082505-6298eb33-ae12-4acd-9601-0027f6f48486.png)

![LASTWORK](https://user-images.githubusercontent.com/118707079/230082530-e57711bf-525c-41a9-9f2b-3fb95808a678.png)

RESULT:

Thus the experiment executed sucessfully.


