# workshop-Multivariate-analysis
# AIM:
To perform multivarient analysis on the given data set.

# ALGORITHM:

1.Clean the data

2.Remove outliers

3.Apply the skew function and Kurtosis

4.Apply Bivariate analysis on numerical and categorical

5.Apply Multivariate analysis.

# CODE:
NAME:NROSHA.S
REG NO:212222230097

## Bivariate Analysis

import pandas as pd
import seaborn as sns
df=pd.read_csv("FlightInformation.csv")
df

df.isnull().sum()

df.info()

df['Route']=df['Route'].fillna(df['Route'].mode()[0])
df['Total_Stops']=df['Total_Stops'].fillna(df['Total_Stops'].mode()[0])
df.isnull().sum()

sns.scatterplot(x=df["Price"],y=df["Airline"],data=df)

sns.boxplot(x=df['SourceSource'],y=df['Price'],data=df)
sns.barplot(x=df['Destination'],y=df['Price'],data=df)

sns.displot(df,x="Destination",hue="Source")

## Multivariate Analysis 

df.corr()import numpy as np

import seaborn as sns
import matplotlib.pyplot as plt
df= pd.read_csv("FlightInformation.csv")
df= np.random.randint(low = 1, high = 100, size = (10,10))
print("The data to be plotted:\n")
print(df)
hm = sns.heatmap(data=df)
plt.show()

# OUTPUT
Bivariate Analysis

# DATA SET

![DSm1](https://user-images.githubusercontent.com/121418437/229786598-af99bdd9-3b22-4554-b9d3-f608d4863791.PNG)

# INFO

![DSm2](https://user-images.githubusercontent.com/121418437/229786690-34e9b5a2-8bd5-405d-8c87-c60d15720b88.PNG)

# DETECTING NULL AS PD

![DSm3](https://user-images.githubusercontent.com/121418437/229786743-73e76732-4b9e-48b7-82b2-88ad587279a8.PNG)

# REMOVING NULL DATA

![DSm4](https://user-images.githubusercontent.com/121418437/229786788-5e16248e-7b0c-4fc3-b87e-d0a5ecd314a6.PNG)

NUMERICAL & NUMERICAL:
# SCATTER_PLOT

![DSm5](https://user-images.githubusercontent.com/121418437/229786915-15dd0fea-1bb1-45b1-9cfe-6141592b6152.PNG)

NUMERICAL & CATEGORIAL:
# BOX PLOT

![DSm6](https://user-images.githubusercontent.com/121418437/229786961-a81b522c-b834-4167-8afb-781bff7a45df.PNG)

# BAR PLOT

![DSm7](https://user-images.githubusercontent.com/121418437/229786999-62588cbf-d11e-4276-841f-5ca172f59d90.PNG)

# DIST PLOT

![DSm8](https://user-images.githubusercontent.com/121418437/229787103-eacbd43b-6445-457a-abed-233842de7649.PNG)

MULTIVARIENT ANALYSIS

# HEAT MAP
![DSm9](https://user-images.githubusercontent.com/121418437/229787152-1655d189-6e13-4f1c-b5e5-ccb65ab090c4.PNG)


# RESULT
   Thus the Bivariate and Multivariate analysis is observerd for the given data set.
