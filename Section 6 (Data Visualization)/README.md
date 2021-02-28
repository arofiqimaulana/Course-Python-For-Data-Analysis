# Data Visualization
Barplot, pie chart, histogram, dan line chart termasuk dalam standard chart. Sedangka stacked, side-by-side, combo, distribution, heatmap, boxplot termasuk dalam advanced chart. Di python terdapat tiga macam package untuk visualisasi data. package seaborn dibangun di atas matloplib, sehingga fitur seaborn lebih tinggi. Sedangkan plotly merupakan interactive chart (terdapat animasi/pergerakan). 

## Matplotlib
```
# Barplot Horizontal
import matplotlib.pyplot as plt
%matplotlib inline

plt.figure(figsize=(8, 8))
plt.barh('city','total',data=df) # Horizontal Plot
plt.title('Total Penduduk Tiap Kota')
plt.show()
```

Other
```
plt.scatter('Assault','Murder',data=df) #Scatterplot
plt.plot('city', 'total',data=df) #Line Chart
plt.pie('total', labels='city', autopct='%1.1f%%',data=df) #Pie Chart 
plt.hist(df.total,bins=30) #Histogram
```


## Seaborn
```
import seaborn as sns
plt.figure(figsize=(8, 8))

sns.set(style="whitegrid")
ax = sns.barplot(x="total", y="city", data=df)
```

Other
```
sns.scatterplot(x="total_bill", y="tip", hue="time",data=tips) #Scatterplot
sns.lineplot(x="timepoint", y="signal", hue="event",data=fmri) #Line Chart

```

## Plotly
```
import plotly.express as px

fig = px.bar(df, x='total', y='city')
fig.show()

```

Other
```
px.scatter(tips,x='total_bill',y='tip') #Scatterplot
px.line(df, x='total', y='city') #Line Chart
px.pie(df, values='total', names='city') # Pie Chart
px.histogram(df, x="total", nbins=30) #Histogram
```



## Refference
1. https://plotly.com/python/bar-charts/
2. https://seaborn.pydata.org/generated/seaborn.barplot.html
3. https://pythonspot.com/matplotlib-pie-chart/