# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages using import statement.
2. Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
3. Import KMeans and use for loop to cluster the data.
4. Predict the cluster and plot data graphs.
5. Print the outputs and end the program.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: JEEVITHA S
RegisterNumber:  212222100016

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers.csv")
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
  kmeans = KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
  plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
### Data.head():
![241356509-13eb30e9-00fb-45a0-a8d6-68e802a446af](https://github.com/Jeevithha/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/123623197/23c1e07b-94a8-4200-93d0-106d3e3f7bab)
### Data.info():
![241356541-7a998261-a53d-442b-9bd9-d66d8475f17d](https://github.com/Jeevithha/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/123623197/7a2a9621-b082-4b14-a22f-3231a97eca4f)
### Data.isnull.sum() function:
![241356629-02aed00f-8ad4-4533-8d13-398f47af667a](https://github.com/Jeevithha/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/123623197/5938d268-8009-4891-af7c-f6d045f55c02)
### Elbow Method Graph:
![241356609-c24c0019-3e36-46c5-9371-990de579961d](https://github.com/Jeevithha/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/123623197/c5bef1bf-2afd-47f7-9cae-b0069f455705)
### KMeans clusters:
![241356760-6dcb359f-0af6-48c1-9f95-6bb2065cb831](https://github.com/Jeevithha/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/123623197/d3c143da-6608-4b61-8618-89bca41c873a)
### Customer Segments Graph:
![241356717-53de6a5b-0333-4028-bdaf-3209e6592b45](https://github.com/Jeevithha/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/123623197/c0d7d320-74a3-4a3b-9784-336cff470b46)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
