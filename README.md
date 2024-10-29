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
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/9f3cfe1f-66d9-44ff-8a2c-8f0533394f07)
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/user-attachments/assets/203ab3bc-2338-4fd3-87a0-a832b44dd7e8)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset("tips")
avg_total_bill=tips.groupby("day")["total_bill"].mean()
avg_tip=tips.groupby('day')["tip"].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/08146922-4923-4f2c-8a87-092c94250628)
```
avg_total_bill=tips.groupby("time")["total_bill"].mean()
avg_tip=tips.groupby("time")["tip"].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/2cb8c794-85ce-4af6-93dc-f7dec2866408)
```
import seaborn as sns
df=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill",hue="sex",data=df,palette="Set1")
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Average Total Bill by Day and Gender')
plt.show()
```
![image](https://github.com/user-attachments/assets/1b76a923-c58f-4f37-ad2f-b624fbaae6c2)
```
import seaborn as sns
tips=sns.load_dataset("tips")
sns.scatterplot(x="total_bill",y="tip",hue="sex",data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Relationship Plot of Total Bill vs. Tip Amount')
plt.show()
```
![image](https://github.com/user-attachments/assets/b73d9611-9ff2-468c-b828-18d2cf870ce3)
```
sns.histplot(data=tips,x="total_bill",hue="smoker",kde=True,palette="Set1")
plt.xlabel('Total Bill')
plt.ylabel('Frequency')
plt.title('Distribution of Total Bill by Gender')
plt.show()
```
![image](https://github.com/user-attachments/assets/a1e54e9a-576b-4eb7-8687-b0b3eac5368d)
![image](https://github.com/user-attachments/assets/9498d570-af08-422d-af95-7e35410b47eb)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
            whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/6ecf274b-7470-4d33-acae-fd7cf3c8e115)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Distribution of Total Bill by Day and Smoker Status')
plt.show()
```
![image](https://github.com/user-attachments/assets/62ce95ec-12ee-414b-9e6f-6944950a9209)
```
import seaborn as sns
sns.set(style ='whitegrid')
tip=sns.load_dataset("tips")
sns.violinplot(x='day',y='tip',data=tip,palette='Set3')
```
![image](https://github.com/user-attachments/assets/c5ab5143-9e86-4c6d-83ff-08ef4a8692c3)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/0dc81e5a-73a4-4b96-b1d1-5c94541c32f8)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)

```
![image](https://github.com/user-attachments/assets/24f37d5f-a56b-4b5c-9605-8a7acf4cf238)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/2c0b6467-d833-47ef-94ec-342786c08bb9)
![image](https://github.com/user-attachments/assets/3a482032-41d4-4954-8221-1fad082ae13d)
![image](https://github.com/user-attachments/assets/be65acc0-64b8-46f3-a4da-c6c763987dd9)
![image](https://github.com/user-attachments/assets/8f0f36d4-2480-4526-93a6-09b762a81a22)

# Result:
 Thus, all the data visualization techniques of seaborn has been implemented.
