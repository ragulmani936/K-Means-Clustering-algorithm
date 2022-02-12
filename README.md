# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:
### Step1
Import pandas,mathplotlib.pyplot,sklearn,seaborn,warnings.

### Step2
Read the csv fileusing df.head() and assign it to the variables

### Step3
Plot the group using scatterplot.

### Step4
Find the centroid using KMeans from sklearn module.

### Step5
Run the program and display the graph.

## Program:
```
## Devloped By: Ragul M
## Register Number:21500303


import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
import seaborn as sns
import warnings
warnings.filterwarnings('ignore')

x1 = pd.read_csv('clustering.csv')
print(x1.head(2))
x2 = x1.loc[:, ['ApplicantIncome', 'LoanAmount']]
print(x2.head(2))

x = x2.values
sns.scatterplot(x[:,0], x[:, 1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()

kmean=KMeans(n_clusters=4)
kmean.fit(x)

print('Cluster Centers:', kmean.cluster_centers_)
print('Labels:', kmean.labels_)

predicted_class = kmean.predict([[9000,120]])
print('The cluster group for Applicant Income 9000 and loanamount 120',predicted_class)





```
## Output:
![output](https://github.com/ragulmani936/K-Means-Clustering-algorithm/blob/master/Screenshot%20(60).png)
![output](https://github.com/ragulmani936/K-Means-Clustering-algorithm/blob/master/Screenshot%20(61).png)

## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.
