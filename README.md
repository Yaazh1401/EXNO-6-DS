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

<img width="751" height="469" alt="image" src="https://github.com/user-attachments/assets/04ccdb2c-bb87-4d5c-af40-3d3e8422e2a8" />

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto",palette="Set1")
```

<img width="1056" height="610" alt="image" src="https://github.com/user-attachments/assets/148218b6-66b1-4ddf-a0e5-bed72043fb00" />


```
x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
plt.show()

```
<img width="945" height="608" alt="image" src="https://github.com/user-attachments/assets/be3a0228-506b-4c13-8f7a-f072cf2d8e8f" />

```
tips= sns.load_dataset("tips")
avg_total_bill = tips.groupby("day")["total_bill"].mean()
avg_tip = tips.groupby("day")["tip"].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label="Total Bill")
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label="Tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
```

<img width="1155" height="716" alt="image" src="https://github.com/user-attachments/assets/73395316-18cf-428f-9b3b-ca8f9eb9c6a6" />

```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label="Total Bill", width=0.4)
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label="Tip", width=0.4)
plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
plt.show()
```
<img width="846" height="575" alt="image" src="https://github.com/user-attachments/assets/cc8d20b7-b12e-450d-8c88-9123b2dee733" />


```
import seaborn as sns
df = sns.load_dataset("tips")
sns.barplot(x="day", y="total_bill", hue="sex", data=df, palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
plt.show()

```

<img width="818" height="593" alt="image" src="https://github.com/user-attachments/assets/d5df5c5a-c8f8-4432-b47a-9d45f350c7a4" />

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.scatterplot(x="total_bill",y="tip", hue="sex", data=df, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
```

<img width="884" height="621" alt="image" src="https://github.com/user-attachments/assets/777161f6-4b80-48e5-b81c-1df6e99d8924" />

```
sns.histplot(data=df, x='total_bill', hue='smoker', kde=True, palette='Set1')
plt.xlabel('Total Bill')
plt.ylabel('Frequency')
plt.title('Distribution of Total Bill by Gender')

```
<img width="885" height="629" alt="image" src="https://github.com/user-attachments/assets/6472e400-9d71-4669-bbdd-d08258c08ba8" />

```
import seaborn as sns
import pandas as pd

df = sns.load_dataset('tips')
sns.boxplot(x='day', y='total_bill', hue='sex', data=df, palette='Set2')

```
<img width="1040" height="614" alt="image" src="https://github.com/user-attachments/assets/f78d0214-2c06-4cd2-801a-e72dcf45f473" />

```
sns.boxplot(x='day', y='total_bill', hue='smoker', data=df, linewidth=2, width=0.6, fliersize=7, flierprops={'marker':'o','markerfacecolor':'grey'}, boxprops={'facecolor':'red','edgecolor':'black'}, whiskerprops={'color':'darkblue','linestyle':'--','linewidth':'-','linewidth':2}, palette='Set1')

```
<img width="980" height="604" alt="image" src="https://github.com/user-attachments/assets/d202b71c-3dc8-47a0-b308-2ed081c98d40" />

```
sns.violinplot(x='day', y='total_bill', hue='smoker', data=tips, linewidth=2, width=0.6, palette='Set1', inner='quartile')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Violin Plot of Total Bill by Day and Smoker Status')

```

<img width="947" height="635" alt="image" src="https://github.com/user-attachments/assets/7abfe15c-b73a-48b7-9bd8-c0ba13d5d063" />

```
import seaborn as sns
sns.set(style='whitegrid')

tip = sns.load_dataset('tips')
sns.violinplot(x='day', y='tip', data=tip, palette='Set2')

```
<img width="907" height="608" alt="image" src="https://github.com/user-attachments/assets/375ccfcf-8b12-4b93-bb53-d9506421365d" />


```
import seaborn as sns
sns.set(style='whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"],palette="Set1")
```
<img width="890" height="614" alt="image" src="https://github.com/user-attachments/assets/90ec9a9c-acbe-413a-be87-a27586989a28" />


```
import seaborn as sns
sns.set(style='whitegrid')
tip= sns.load_dataset('tips')
sns.violinplot(x='tip', y='day', data=tip, palette='rainbow')

```


```
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='layer', linewidth=3, palette='Set2', alpha=0.8)

```


```
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set3', alpha=0.8)

```

```
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='fill', linewidth=3, palette='Set1', alpha=0.8)

```

```
import seaborn as sns
tip= sns.load_dataset('tips')
num = tips.select_dtypes(include=['float64', 'int64']).columns
corr = tips[num].corr()
sns.heatmap(corr, annot=True, cmap='YlGnBu')

```

```
sns.heatmap(corr,cmap="YlGnBu")
```






# Result:
Thus, all the data visualization technique has been impleamented
