# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("titanic_dataset.csv")
 df.head()

```
<img width="1563" height="277" alt="image" src="https://github.com/user-attachments/assets/aea0189a-f7d6-48da-924d-4b7c8fdc67e0" />

```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```
<img width="534" height="435" alt="image" src="https://github.com/user-attachments/assets/ec72975d-5b68-485b-9369-3136856ed851" />

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
<img width="534" height="435" alt="image" src="https://github.com/user-attachments/assets/5eced25c-42a6-4bb6-b90c-879753dcaf47" />

```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```
<img width="901" height="601" alt="image" src="https://github.com/user-attachments/assets/d7249ae9-0eb1-4c66-b7e9-919fd990236c" />


```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```
<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/0d451c6c-bcd0-465e-9f30-49fdf2645f7b" />

```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```
<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/8a4a3523-ed38-47ee-96e6-8cfb376d86db" />

```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/cd393cdd-3c54-4ffb-b6fa-244a3359ea09" />


```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```
<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/86d09213-73e9-4b0c-a2c4-e44b88f73fd3" />

```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```
<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/27c2f151-d58f-4a47-9200-0268131c0b13" />


```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```
<img width="584" height="455" alt="image" src="https://github.com/user-attachments/assets/65cefae2-a7a0-4f03-a8e5-11cc5cfa558e" />


```

``` numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```

<img width="596" height="505" alt="image" src="https://github.com/user-attachments/assets/e6363b0b-bfdb-48ba-851e-21bc5f27ea89" />

# Result:

 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
