# Conditional & Looping

## A. Conditional
1. Conditional execution

```
# statement if
if x > 8:
    print('Good')
```

```
# statement if else
if x > 8:
    print('Good')
else:
    print('Bad')
```

2. Chained conditionals

```
# statement if elif else
if x <= 8 :
    print 'Bad'
elif (x > 8) & (x < 12):
    print('Enough')
else:
    print('Good')
```

3. Nested conditionals
```
# statement if inside in if
if x < y:
    print('Good')
else:
    if x > y :
        print('Bad')
    else:
        print('Same')
``` 

## B. Looping
tim = ['liverpool','ac milan','juventus','arsenal','Barcelona']

```
# looping using index
for k in range(len(tim)):
    print(tim[k])

# looping using item list
for k in tim:
    print(k)

# list comprehension (pythonic)
[k for k in tim]
```



