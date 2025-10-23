# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Name: RAGHUL S
Reg.no: 212222040128
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1372" height="467" alt="image" src="https://github.com/user-attachments/assets/72b75445-0894-40d5-8295-9238d8f960ad" />



### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="808" height="692" alt="image" src="https://github.com/user-attachments/assets/ea4553dd-f5fe-49d3-a1a0-1efa9354b5c1" />


### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="807" height="735" alt="image" src="https://github.com/user-attachments/assets/3ba95aea-619f-4e12-98e1-7ea9e0a14109" />



## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="901" height="712" alt="image" src="https://github.com/user-attachments/assets/85fc6356-fdf8-4f0b-bd94-f2e643998a85" />


### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="737" height="690" alt="image" src="https://github.com/user-attachments/assets/e129add3-6f63-46c7-ba37-af0d56e5faa2" />


### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="778" height="687" alt="image" src="https://github.com/user-attachments/assets/d5032524-483e-4eab-a1a5-64e396345aeb" />


## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="781" height="638" alt="image" src="https://github.com/user-attachments/assets/01ed87ff-7720-4717-a7b2-a30ce5fcb29c" />


### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="1131" height="732" alt="image" src="https://github.com/user-attachments/assets/7e61146e-6b00-4332-ac2e-021f7ace53a3" />


### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="767" height="680" alt="image" src="https://github.com/user-attachments/assets/d355329b-21ad-4f6f-8ad1-14de32af3b18" />


### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="782" height="735" alt="image" src="https://github.com/user-attachments/assets/c061e185-822f-4ec2-8c74-a2cbf2d23b80" />
 

### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="787" height="730" alt="image" src="https://github.com/user-attachments/assets/d71477e9-1740-4f2a-8fa8-2380fcdf6ee3" />


## Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
