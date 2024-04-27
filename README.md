# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
Developed by : SUDHIR KUMAR .R
Register number : 212223230221
```
```
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```

![324162986-d83ea26b-0be7-42f2-ac05-23f7be976ac5](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/48e1f63b-3409-4963-9845-756798caa53e)

### 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

![324162989-f0d7d503-3f08-41e4-a2a0-4151ab5c2cb8](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/a975ba75-e1f0-4530-8b91-4523323796eb)

### 2.Multi Line Plot
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

![324162996-d4c830c1-17e2-4533-a5bf-9125b002c47b](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/47f43be5-b1dc-4574-b18b-0e7e9efbf46c)

## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

![324163001-d8824a6e-d89e-4469-9aaf-74ee16c4e961](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/fc595ef9-8287-4526-8620-4bbf4cbffb53)

### 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

![324163007-78b9ffbd-cc91-4f6a-b41a-c367b83062f7](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/fcd466e7-816b-4c39-9a27-5a62333aefa9)

### 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

![324163011-bd9c1f59-b33b-4869-aa5a-0ee876a7c8ab](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/0ae948a5-8b81-4c87-81d3-4119f2776bfe)

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

![324163016-bca9a8b5-ad6d-4488-89bc-8fe7fdcb4967](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/210e066f-ba06-4a66-af82-a9f8036ea826)

### 2.Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

![324163023-95bb6d12-2723-432d-a50a-6db241a68633](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/58491c35-1e18-4ae9-9f14-667447ceaef0)

### 3.Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

![324163027-a449378c-ebf5-416b-901c-3110875651ef](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/155dc023-007e-462e-9391-ca4f51701058)

### 4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

![324163034-c2945da4-34fe-4526-8fcb-63df89686fe9](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/152b3122-30b8-4b3b-9d60-92c1b41aa4a1)

### 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

![324163036-e3abb871-9cba-4007-b9fd-03c5e007347d](https://github.com/Sudhirr5/EXNO-6-DS/assets/139332214/d77526de-c43c-4d3f-9200-148327ae03e7)

# Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
