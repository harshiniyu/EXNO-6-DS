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
## Name:Harshini Y
## reg no:212223240050
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
```
```
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/55182cc6-1f5b-42ea-8297-49ddd75aba74)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/d5d448fa-f686-40d1-beae-a6f50623f555)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/user-attachments/assets/8c316cd7-964a-4de2-9636-28c357df96d7)
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
![image](https://github.com/user-attachments/assets/323ce805-35b1-450c-a40b-ddc453151ebe)
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
![image](https://github.com/user-attachments/assets/19f0b105-bbee-4d3c-afc6-669d3758954a)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/user-attachments/assets/7f7c4853-2c7e-4af1-b1f4-d25a97121d28)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/user-attachments/assets/732ef13e-fe3e-4ec1-8a75-574f7240646d)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/b516161c-bb4d-4ba5-b0fa-a88e43f3811b)
```
tit=pd.read_csv("/content/titanic_dataset (2).csv")
tit
```
![image](https://github.com/user-attachments/assets/cee76749-065b-4d03-8824-fbd212206b54)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/f834e0a6-4ca6-45b1-9318-3e32ea79b73c)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/67e77c30-2196-4773-aac2-ce64d628b505)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/c754ce03-4b11-40ed-b249-b9d7f8985378)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/409641dd-4798-4a1d-9194-4a1d02ac38c3)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/62290a42-bbf8-463f-8bea-2783823a5070)
```
df=pd.read_csv("/content/titanic_dataset (2).csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/b6ab44b9-3e0c-46a5-a885-907aac96d448)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/c285acb6-45c8-4e20-a5a3-dbe4813d27aa)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/882316d3-d9f9-493e-93c9-e3023a4218d2)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![image](https://github.com/user-attachments/assets/51705268-a9ac-409d-a186-5b5e0cdcf1ee)
```
mart=pd.read_csv("/content/titanic_dataset (2).csv")
mart
```

![image](https://github.com/user-attachments/assets/8416a921-274d-455b-9690-2b7248cd5e71)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```

![image](https://github.com/user-attachments/assets/6008eb25-239d-4bc4-aa5c-96c5a5307515)
```
sns.kdeplot(data=mart,x='PassengerId')
```

![image](https://github.com/user-attachments/assets/5a5e58a3-0fc8-4e7c-a10f-383394cebdce)
```
sns.kdeplot(data=mart,x='Age')
```

![image](https://github.com/user-attachments/assets/caf394de-6c5b-4083-8c0b-2ae39922cd73)
```
sns.kdeplot(data=mart)
```

![image](https://github.com/user-attachments/assets/e4c9fc58-0f65-4542-9b78-8f8100900d23)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

![image](https://github.com/user-attachments/assets/cea519be-9a46-4cec-8c29-0797737379cf)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

![image](https://github.com/user-attachments/assets/32961a5d-341c-4f41-99be-f9e268ff7c8c)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

![image](https://github.com/user-attachments/assets/1459edc1-e6e5-408b-90c2-f845160d87b5)
```
hm=sns.heatmap(data=data)
```

![image](https://github.com/user-attachments/assets/8bc90270-4056-4bad-bd8b-3dd9e1d2edc5)

# Result:
Thus data Visualization using seaborn python library for the given datas is performed.
