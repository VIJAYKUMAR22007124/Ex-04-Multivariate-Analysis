# Ex-04-Multivariate-Analysis

AIM:

To perform various operations of multivariate analysis in the given dataset.

ALGORITHM:

A dataset("SuperStore.csv") is given , use that and perform the multivariate operations in the colab and get the output in graph models. 

CODE:

```
import pandas as pd 
import seaborn as sns
import matplotlib as plt
df = pd.read_csv("SuperStore.csv")
print(df)

df.corr()

print(sns.scatterplot(df["Postal Code"]))

sns.barplot(x = df['Postal Code'], y=df['Sales'],data = df)

GRAPH = df.loc[:,['Region','Sales']]
GRAPH=GRAPH.groupby(by=["Region"]).sum().sort_values(by="Sales")
sns.barplot(x=GRAPH.index,y="Sales",data=GRAPH)

plt.xlabel=("Region")
plt.ylabel=("Sales")

df.info()
df.describe()

GRAPH = df.loc[:,['Postal Code','Sales']]
GRAPH=GRAPH.groupby(by=["Postal Code"]).sum().sort_values(by="Sales")
sns.barplot(x=GRAPH.index,y="Sales",data=GRAPH)

plt.xlabel=("Postal Code")
plt.ylabel=("Sales")

sns.barplot(x = df['Postal Code'], y=df['Sales'],hue = df['Region'])

sns.heatmap(df.corr(),annot=True)

```

OUTPUT:

![Screenshot (273)](https://user-images.githubusercontent.com/119657657/229834596-fcb67584-f891-4d15-882e-6e672ae44074.png)

![Screenshot (274)](https://user-images.githubusercontent.com/119657657/229834725-effe3f0f-8b19-4934-8825-0b1f88151aec.png)

![Screenshot (275)](https://user-images.githubusercontent.com/119657657/229834880-13f4231c-7f15-48e6-81b3-96c07a11fb93.png)

![Screenshot (276)](https://user-images.githubusercontent.com/119657657/229835006-c004d3f9-dcf7-4d82-947c-57502092e7d2.png)

![Screenshot (277)](https://user-images.githubusercontent.com/119657657/229835120-4eced88f-86c5-42e2-93de-3792c89e0cae.png)

![Screenshot (278)](https://user-images.githubusercontent.com/119657657/229835206-24e73e72-55c9-42a2-845a-4146c9e81788.png)

![Screenshot (279)](https://user-images.githubusercontent.com/119657657/229835540-e8a5fa17-b11f-4784-b6b6-5885242cc572.png)

![Screenshot (280)](https://user-images.githubusercontent.com/119657657/229835687-4a2ae946-96ed-4c61-a5a3-101a40c27f80.png)

![Screenshot (281)](https://user-images.githubusercontent.com/119657657/229835949-68e0f87f-40e8-46fd-a5c2-746c51729acc.png)

RESULT:

      Operations are done on the given dataset based on the multivariate analysis.








