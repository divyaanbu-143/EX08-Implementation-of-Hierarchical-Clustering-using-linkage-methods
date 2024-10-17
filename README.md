# EX8-Implementation of Hierarchical Clustering using linkage methods
## DATE:
## AIM:
To implement Hierarchical Clustering using single and complete linkage method

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Compute the distance matrix between all data points.

2.Identify the two closest cluster and merge them.

3.Update the distance matrix to reflect the new cluster.

4.Repeat steps 2 and 3 until only one cluster remains.







## Program:
```
Program to implement Hierarchical Clustering using single and complete linkage method
Developed by: Divya A
RegisterNumber: 2305002007
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt 
from scipy.cluster.hierarchy import dendrogram, linkage, fcluster 
from sklearn.preprocessing import StandardScaler
df=pd.read_csv("/content/Hclus_EX8.csv")
df.head()
X=df[['StudentID','Marks']].values
X
Z=linkage(X,method='complete')
plt.figure(figsize=(5,2))
plt.title("Dentogram for Student Segmentation")
labels=range(1,len(df)+1)
dendrogram(Z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
max_clusters=2
clusters=fcluster(Z,max_clusters,criterion='maxclust')
clusters
plt.figure(figsize=(5,2))
plt.scatter(X[:,0],X[:,1],c=clusters,cmap='rainbow',s=100)
plt.title("Student Segmented (Hierarchical Clustering)")
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
Z=linkage(X,method='single')
plt.figure(figsize=(5,2))
plt.title("Dentogram for Student Segmentation")
labels=range(1,len(df)+1)
dendrogram(Z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
max_clusters=2
clusters=fcluster(Z,max_clusters,criterion='maxclust')
clusters
plt.figure(figsize=(5,2))
plt.scatter(X[:,0],X[:,1],c=clusters,cmap='rainbow',s=100)
plt.title("Student Segmented (Hierarchical Clustering)")
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show() 
```

## Output:

![image](https://github.com/user-attachments/assets/946b7215-7463-4f90-b6d1-4a524f55cfe3)
![image](https://github.com/user-attachments/assets/c9a8ab9a-651e-46b0-874b-6ce3cf3547fd)
![image](https://github.com/user-attachments/assets/3870aa71-6af4-47d0-96b9-4144bc37dc9f)
![image](https://github.com/user-attachments/assets/01ce1c04-067d-42be-870d-05773f353698)
![image](https://github.com/user-attachments/assets/672a8cde-eb25-438b-8870-6b3e0fc4135e)



## Result:
Thus the implementation of Hierarchical Clustering using single and complete linkage method in python programming and verified successfully.
