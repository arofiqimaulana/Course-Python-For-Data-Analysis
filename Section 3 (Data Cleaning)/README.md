# Data Transformation
Berfungsi untuk mengubah suatu format data ke format yang lain sesuai yang diinginkan, seperti group by, filter, join, union dan lainnya.

## 1. DataFrame
#### Select Columns
```
# select one column
df['userid'] 
df.userid 

# select two or more columns
df[['userid','total']]
df.iloc[:,3:5] # select columns 4th until 5th 
```
#### Select Rows
```
#select rows first until 4th
df.iloc[1:4,:] 
df[1:4]
```

#### Filter
```
df[df['userid']==120]
df[(df['age']== 32) & (df['city']=='Manchester')]

#alternatif
df[df.userid==120]
df[(df.age ==32) & (df.city =='Manchester')]

```

#### Groupby
```
df[['userid','city']].groupby(['city']).count()
df[['userid','city']].groupby(['city']).sum()
df[['userid','city']].groupby(['city']).mean()
```

#### Sort values
```
df.sort_values(by=['total'],ascending = False,inplace=True)
```

#### Join
```
pd.merge(df1,df2,on='userid',how='inner')

df1.merge(df2,left_on='userid',right_on='id',how='inner')
```

#### Union
```
pd.concat([df1,df2],axis=0,ignore_index=True) # union by rows

pd.concat([df1,df2],axis=1,ignore_index=True) # union by columns
```

#### IN, NOT IN
```
df[df.relid.isin(userid)] # IN userid list
df[~df.relid.isin(userid)] # NOT IN userid list
```

#### Apply Function
```
df['userid'].apply(CleaningCity)
```

#### Fill NA
```
df.fillna('',inplace=True)
```

## 2. String
```
s.lower()
s.upper()
s.strip()
s.lstrip()
s.rstrip()
s.split()
s.find()
s.replace()
```

## 3. List

```
'org' in ['com','id','org']
[1,2,3] + [4,5]
['abc','def']*4
index()
count()
sort()
append()
[k for k in temp if k not in ['a','b']]
["hello" for _ in range(len(adj))]
```

