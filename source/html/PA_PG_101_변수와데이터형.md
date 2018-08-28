
# Industry 4.0 의 중심, BigData

<div align='right'><font size=2 color='gray'>Data Processing Based Python @ <font color='blue'><a href='https://www.facebook.com/jskim.kr'>FB / jskim.kr</a></font>, 김진수</font></div>
<hr>

## Python PG Section 1

<div><font color='brown' size='3'><b>화면에 출력하기</b></font></div>

#### 문자 출력


```python
print('Hello, Python !!')
```

    Hello, Python !!
    


```python
print('안녕하세요.\n파이썬세계로 온것을 환영합니다.')
```

    안녕하세요.
    파이썬세계로 온것을 환영합니다.
    


```python
print('''
파이썬과정을 통해
데이터를 자유자제로 다룰수 있기를 바랍니다.
끝까지 화이팅하세요!!!
''')
```

    
    파이썬과정을 통해
    데이터를 자유자제로 다룰수 있기를 바랍니다.
    끝까지 화이팅하세요!!!
    
    

#### 숫자 출력


```python
print(100)
```

    100
    


```python
print(150 + 200)
print(150 - 200)
```

    350
    -50
    


```python
print(150. + 200)
print(150. - 200)
```

    350.0
    -50.0
    

* 변수


```python
name = '홍길동'
greeting = '안녕'
```


```python
print(name, greeting)
print(greeting, name)
```

    홍길동 안녕
    안녕 홍길동
    


```python
text = name + '님, ' + greeting + '하세요'
print(text)
```

    홍길동님, 안녕하세요
    


```python
coffee1_name = '카페라떼';  coffee1_val = 4000;
coffee2_name = '카푸치노';  coffee2_val = 4500;
coffee3_name = '마끼야또';  coffee3_val = 5000;
```


```python
print('손님, ' + coffee1_name + coffee2_name + coffee3_name + '를 주문하셨습니다.')
print('가격은 ' + coffee1_val + coffee2_val + coffee3_val + '원 입니다.')
```

    손님, 카페라떼카푸치노마끼야또를 주문하셨습니다.
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-11-dd6755975de7> in <module>()
          1 print('손님, ' + coffee1_name + coffee2_name + coffee3_name + '를 주문하셨습니다.')
    ----> 2 print('가격은 ' + coffee1_val + coffee2_val + coffee3_val + '원 입니다.')
    

    TypeError: must be str, not int



```python
print('손님, ' + coffee1_name + coffee2_name + coffee3_name + '를 주문하셨습니다.')
print('가격은 ' + str(coffee1_val + coffee2_val + coffee3_val) + '원 입니다.')
```

    손님, 카페라떼카푸치노마끼야또를 주문하셨습니다.
    가격은 13500원 입니다.
    


```python
# 출력1
print('손님, \n' + coffee1_name + ', '+ coffee2_name + ', ' + coffee3_name + '를 주문하셨습니다.')
print('가격은 ' + str(coffee1_val + coffee2_val + coffee3_val) + '원 입니다.')
```

    손님, 
    카페라떼, 카푸치노, 마끼야또를 주문하셨습니다.
    가격은 13500원 입니다.
    


```python
coffee_val = coffee1_val + coffee2_val + coffee3_val
```


```python
# 출력2
print('손님, \n%s, %s, %s를 주문하셨습니다.' % (coffee1_name, coffee2_name, coffee3_name))
print('가격은 %d원 입니다.' % coffee_val)
```

    손님, 
    카페라떼, 카푸치노, 마끼야또를 주문하셨습니다.
    가격은 13500원 입니다.
    


```python
# 출력3
print('손님, \n{}, {}, {}를 주문하셨습니다.\n가격은 {}원 입니다.'.format(
    coffee1_name, coffee2_name, coffee3_name, coffee_val
))
```

    손님, 
    카페라떼, 카푸치노, 마끼야또를 주문하셨습니다.
    가격은 13500원 입니다.
    

<font color='brown'>
### 키보드로 입력받기


```python
name = input('당신의 이름은 무엇입니까? ')
```


```python
print(name + '님, 반갑습니다.')
```

    하나님, 반갑습니다.
    


```python
order = input('DD카페입니다. \n무엇을 주문하시겠습니까? ')
count = input('몇 잔을 드릴까요? ')
```


```python
print('%s %s잔을 주문하셨습니다. \n잠시만 기다려주세요~^^' % (order, count))
```

    아메리카노 2잔을 주문하셨습니다. 
    잠시만 기다려주세요~^^
    


```python
price = 2500
cost  = price * count

print('%s %s잔을 주문하셨습니다. \n결재하실 금액은 %s원입니다~^^' % (order, count, cost))
```

    아메리카노 2잔을 주문하셨습니다. 
    결재하실 금액은 2222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222원입니다~^^
    


```python
price = 2500
cost  = price * int(count)

print('%s %s잔을 주문하셨습니다. \n결재하실 금액은 %d원입니다~^^' % (order, count, cost))
```

    아메리카노 2잔을 주문하셨습니다. 
    결재하실 금액은 5000원입니다~^^
    

<font color='brown'>
### 숫자형 데이터


```python
x = 20
y = 5.

print("x = ", x)
print("y = ", y)
print("x + y = " , x+y)
print("x - y = " , x-y)
print("x * y = " , x*y)
print("x / y = " , x/y)
print("x //y = " , x//y)
print("x % y = " , x%y)
print("-x = "    , -x)
print("+x = "    , +x)
print("x**y = "  , x**y)
print("pow(x,y) = ", pow(x,y))
```

    x =  20
    y =  5.0
    x + y =  25.0
    x - y =  15.0
    x * y =  100.0
    x / y =  4.0
    x //y =  4.0
    x % y =  0.0
    -x =  -20
    +x =  20
    x**y =  3200000.0
    pow(x,y) =  3200000.0
    

<font color='brown'>
###  불린형 데이터


```python
# 비교연산자와 논리연산자
x = 2
y = 3

print("x == y = ", x==y)
print("x != y = ", x!=y)

print("x < y  = ", x<y)
print("x > y  = ", x>y)

print("int(True)  = ", int(True))
print("int(False) = ", int(False))

```

    x == y =  False
    x != y =  True
    x < y  =  True
    x > y  =  False
    int(True)  =  1
    int(False) =  0
    


```python
a = True
b = False

print(a == 1)        # True가 출력됨
print(b != 0)        # False가 출력됨
```

    True
    False
    


```python
# 관계 연산자 (==, !=, ＜, ＜=, ＞, ＞=)
x = 100;  y = 200
str1 = 'java'; 
str2 = 'python'

print(x == y)
print(x != y)
print(str1 == str2)
print(str2 == 'python')
print(str1 < str2)
```

    False
    True
    False
    True
    True
    


```python
# 논리 연산자 (and, or, not)
bool1 = True; bool2 = False; 
bool3 = True; bool4 = False

print(bool1 and bool2)
print(bool1 and bool3)
print(bool2 or bool3)
print(bool2 or bool4)
print(not bool1)
print(not bool2)
```

    False
    True
    True
    False
    False
    True
    

<font color='brown'>
###  문자형 데이터


```python
message = """# 두가지 장벽 뛰어넘기
1.디버깅극복 : 무조건 실행시킨다
2.안보고코딩 : 혼자서 작성해본다

'모르는건 언제든 질문하기'
"절대로 포기하기 없기"
"""
print(message)
```

    # 두가지 장벽 뛰어넘기
    1.디버깅극복 : 무조건 실행시킨다
    2.안보고코딩 : 혼자서 작성해본다
    
    '모르는건 언제든 질문하기'
    "절대로 포기하기 없기"
    
    


```python
test = '파이썬 프로그래밍은 재미있어요!'    # 문자열을 변수에 저장

result = test.startswith('파이썬')          # 문자열이 '파이썬으로 시작하는지 확인
print(result)
result = test.endswith('!')               # 문자열이 '!'로 끝나는지 확인
print(result)
result = test.endswith('어려워요!')          # 문자열이 '어려워요!'로 끝나는지 확인
print(result)
result = test.replace('파이썬', 'Python')   # 문자열중 '파이썬'을 'Python'으로 변경
print(result)

```

    True
    True
    False
    Python 프로그래밍은 재미있어요!
    


```python
test = 'Python Programming is Interesting!'
test = 'Life is too short. You need python!'

result = test.upper()        # 문자열을 모두 대문자로 변경
print(result)
result = test.lower()        # 문자열을 모두 소문자로 변경
print(result)
result = '/'.join(test)      # 문자열의 각 문자 사이에 '/'문자 집어 넣기
print(result)

```

    LIFE IS TOO SHORT. YOU NEED PYTHON!
    life is too short. you need python!
    L/i/f/e/ /i/s/ /t/o/o/ /s/h/o/r/t/./ /Y/o/u/ /n/e/e/d/ /p/y/t/h/o/n/!
    

<hr>
<div>
<marquee><font size=3 color='brown'>The BigpyCraft find the information to design valuable society with Technology & Craft.</font></marquee>
</div>
<div align='right'><font size=2 color='gray'> &lt; The End &gt; </font></div>
