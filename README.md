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
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![1](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/06716a30-abca-42d3-a232-b52c928d9157)


```
df = sns.load_dataset("tips")
df
```
![2](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/2c2cd967-0d83-4c51-8ff2-215181a5e009)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![3](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/85ac18d4-fa64-40f7-b4ae-a9be767fad5c)


```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![4](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/46c85719-06ec-415a-89bd-e8784b0a2789)

```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![5](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/0022e244-6272-4aa9-a242-18a06d0e3c6e)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![6](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/071f0220-7f8e-43c2-b398-d122be11d435)


```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![7](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/f0bd02b6-a928-4ec6-82df-86480a73ba35)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![8](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/5608dfc4-2245-403c-bf8a-0383a70d203b)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![9](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/0b0fb982-6680-43fc-91cd-a0e342bd0a2c)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![10](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/88c91c48-0d2f-4c0d-bfd4-0323cb2c55c4)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![11](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/e63bfadf-2363-4771-a335-f32f78da1d50)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![12](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/b5e5656f-3e5a-4ced-93e6-efdaa54d7957)



```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![13](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/fb99fd75-dc47-465f-9c9a-ad5613b908d7)


```
sns.histplot(data = num_var, kde = True)
```
![14](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/ad1e8837-63fc-404e-97fd-945da64906c2)


```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![16](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/40b3f28f-475c-40a6-9fa0-a4adb4a71e17)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![17](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/2c31ebd5-bd6b-4ffe-8da1-f97ecf3b9d60)


```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![18](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/cbe10088-d201-4f9b-b10d-d851147551e7)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![19](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/3d3b0fec-f019-406d-b182-83d398c96840)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![20](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/72149b0f-a703-4e2a-981d-1fde85d472c1)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![21](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/45fe0842-08ee-4a4d-8489-5a6fdf87db0e)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![22](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/62a9b26c-ec78-43f2-8950-b027eca838cc)

```
sns.kdeplot(data=mart,x='Age')
```
![33](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/5b28e9d8-3ec6-42cd-b21c-4d4985594015)


```
sns.kdeplot(data=mart)
```
![24](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/19631b56-ed1b-4e6b-adeb-c8d6b826f897)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![25](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/dae1b783-b3ec-4807-b008-7945d404f8df)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![26](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/c65ec0d2-f746-484f-b581-c5363787d7e2)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![27](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/d46c798d-ae68-46e4-8652-c4e7c9a25f4f)


```
hm=sns.heatmap(data=data)
```
![28](https://github.com/VISHVA12300/EXNO-6-DS/assets/119404426/6c8958b6-5ff5-4bd9-bf45-b600f3854f4f)


# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
