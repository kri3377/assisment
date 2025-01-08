import pandas as pd
import seaborn  as sns
import matplotlib.pyplot as plt
def load_dataset(file_path):
  return pd.read_xlsvv(file_path)


df = pd.read_excel('one.xlsx', engine='openpyxl')
df.head(5)

sns.countplot(data=df, x='BMI')
df['age'].value_counts()
df['sex'].value_counts().plot(kind='pie',autopct='%0.2f')
#Numberical Value

# Histogram treat as categorical data distribution of data

plt.hist(df['age'])
sns.histplot(df['age'], kde=True)

# Boxplot
# 5 number summary
# median , percentile, min=Q1-1.5*IQR, max=Q3+1.5*IQR, IQR = (Q1-Q3), outlier

sns.boxplot(df['age'])
df.describe()
# lineplot(Numerical - Numerical)
flight.head()

flight = sns.load_dataset('flights')
flight
iris = sns.load_dataset('iris')
iris
# Scatter plot(Numerical - Numerical) for the relation between two column
sns.scatterplot(x='total_bill', y='tip',hue='sex', style='smoker',size='size' ,data=tips)
plt.show()
# Bar plot (Numerical - Categorical)
  # average age in pclass
sns.barplot(x='sex', y='BMI', hue='indication', data=df)

#Box plot (Numerical - Categorical)

sns.boxplot(x='sex',y='age',hue='BMI',data=df)
# Displot

sns.histplot(df[df['indication']==0]['BMI'], kde=False)
sns.histplot(df[df['indication']==1]['BMI'],kde=False)
# HeatMap (Categorical - Categorical)
sns.heatmap(pd.crosstab(df['age'],df['indication']))
df.groupby('age').mean()['indication']*100
# pairplot
sns.pairplot(iris,hue='species')
new = flight.groupby('BMI').sum().reset_index()

sns.lineplot(x='age',y='indication',data=df)
sns.heatmap(flight.pivot_table(values='age',index='month',columns='year'))
print(df['age'])

sns.clustermap(flight.pivot_table(values='passengers',index='month',columns='year'))
tips = sns.load_dataset('tips')
tips
# Scatter plot(Numerical - Numerical) for the relation between two column
sns.scatterplot(x='total_bill', y='tip',hue='sex', style='smoker',size='size' ,data=tips)
plt.show()
     
