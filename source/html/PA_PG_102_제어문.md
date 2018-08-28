
<center>
<b><font size=6>Industry 4.0 의 중심, BigData</font></b>
</center>

<div align='right'><font size=2 color='gray'>Data Processing Based Python @ <font color='blue'><a href='https://www.facebook.com/jskim.kr'>FB / jskim.kr</a></font>, 김진수</font></div>
<hr>

# Industry 4.0 의 중심, BigData

# Python PG Section 2

<font color='brown'>
### 조건문, if 


```python
condition = True

if condition:
    print("조건을 충족함, condition met")
```

    조건을 충족함, condition met
    


```python
if not condition:
    print("조건 충족 못함, condition not met")
```


```python
num_a = 100
num_b = 200

if num_a == num_b:
    print('숫자A와 숫자B는 같습니다.')
else:
    print('숫자A와 숫자B는 같지않습니다.')
```

    숫자A와 숫자B는 같지않습니다.
    


```python
x = 10
y = 20

if x > y:
    print('x가 y보다 큽니다.')
else:
    print('x가 y보다 작거나 같습니다.')

```

    x가 y보다 작거나 같습니다.
    


```python
# 010 if문 개념 배우기 ② (if~elif)
x = 10
y = 20

if x > y:
    print('x가 y보다 큽니다.')
elif x < y:
    print('x가 y보다 작습니다.')
else:
    print('x와 y가 같습니다.')
```

    x가 y보다 작습니다.
    


```python
score = 75
grade = ''

if 90 <= score and score <= 100:
    grade = 'A'
    
if 80 <= score and score < 90:
    grade = 'B'
    
if 70 <= score and score < 80:
    grade = 'C'
    
if 60 <= score and score < 70:
    grade = 'D'
    
if score < 60:
    grade = 'F'

print('시험의 결과는 ' + grade + '입니다.')
```

    시험의 결과는 C입니다.
    


```python
score = 88
grade = ''

if 90 <= score:
    grade = 'A'  
elif 80 <= score:
    grade = 'B'
elif 70 <= score:
    grade = 'C'
elif 60 <= score:
    grade = 'D'
else:
    grade = 'F'

print('시험의 결과는 ' + grade + '입니다.')
```

    시험의 결과는 B입니다.
    


```python
# 주의
score = 95
grade = ''

if 60 <= score:
    grade = 'D'  
elif 70 <= score:
    grade = 'C'
elif 80 <= score:
    grade = 'B'
elif 90 <= score:
    grade = 'A'
else:
    grade = 'F'

print('시험의 결과는 ' + grade + '입니다.')
```

    시험의 결과는 D입니다.
    

<font color='brown'>
### 순환문, for 


```python
scope = [1, 2, 3, 4, 5]
for x in scope:
    print(x)
```

    1
    2
    3
    4
    5
    


```python
scope = [1, 2, 3, 4, 5]
for x in scope:
    print(x)
    if x < 3:
        continue
    else:
        break
```

    1
    2
    3
    


```python
scope = [1, 2, 3, 4, 5]
for x in scope:
    print(x)
    if x < 3:
        print('Meet the continue')
        continue
    else:
        print('Meet the break')
        break
    print('End of for')

print('End of PG')
```

    1
    Meet the continue
    2
    Meet the continue
    3
    Meet the break
    End of PG
    


```python
scope = [1, 2, 3]
for x in scope:
    print(x)
    break
else:
    print('Perfect')
```

    1
    


```python
#중첩 for문
next = [[1, 2, 3],
        [4, 5, 6],
        [7, 8, 9]]

for x in range(3):
    for y in range(3):
        print('next[%d][%d] : %d' % (x, y, next[x][y]))

```

    next[0][0] : 1
    next[0][1] : 2
    next[0][2] : 3
    next[1][0] : 4
    next[1][1] : 5
    next[1][2] : 6
    next[2][0] : 7
    next[2][1] : 8
    next[2][2] : 9
    

<font color='brown'>
### 순환문, while


```python
x = 1
total = 0
while 1:
    total = total + x
    if total > 100000:
        print(x)
        print(total)
        break
    x = x + 1
    
```

    447
    100128
    


```python
x = 0
while x < 10:
    x = x+1
    if x < 3:
        continue
    print(x)
    if x > 7:
        break
        
```

    3
    4
    5
    6
    7
    8
    

<hr>
<marquee><font size=3 color='brown'>The BigpyCraft find the information to design valuable society with Technology & Craft.</font></marquee>
<div align='right'><font size=2 color='gray'> &lt; The End &gt; </font></div>
