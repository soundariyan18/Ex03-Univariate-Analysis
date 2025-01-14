# Ex03-Univariate-Analysis

## AIM:

To read the given data and perform the univariate analysis with different types of plots.

EXPLANATION:

Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

## ALGORITHM:

Step 1:

Read the given data.

Step 2:

Get the information about the data.

Step 3:

Remove the null values from the data.

Step 4:

Mention the datatypes from the data.

Step 5:

Count the values from the data.

Step 6:

Do plots like boxplots,countplot,distribution plot,histogram plot.

## PROGRAM:

NAME: SOUNDARIYAN M.N

REG: 212222230146

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

import seaborn as sns
df=pd.read_csv("iris.csv")
df.head()

df.tail()

df.nunique()

df.iloc[:,4].value_counts()
for i in range(0,df.shape[1]):

  print("-----------",df.columns[i],"------------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------------")

sns.countplot(x='species',data=df)

dfv=df.loc[df['species']=='virginica']
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()

dfs=df.loc[df['species']=='setosa']
dfc=df.loc[df['species']=='versicolor']

plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'X')
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'X')
plt.xlabel('petal_length')
plt.show()

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()




## OUTPUT:
```
df.head()

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155508.png)

df.tail()

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155539.png)

df.nunique()

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155553.png)

df.iloc()

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155604.png)


Sepal


![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155657.png)
![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155726.png)
![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155811.png)
![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155907.png)



Countplot

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155918.png)

dfv

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155931.png)

dfs

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20155944.png)

petal_length

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20160001.png)

sepal_length

![MODEL](https://github.com/soundariyan18/Ex03-Univariate-Analysis/blob/main/Screenshot%202023-09-09%20160012.png)
```
RESULT:

The given datasets are read and outliers are detected and are removed using IQR and z-score methods.
