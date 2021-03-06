
# Industry 4.0 의 중심, BigData

<div align='right'><font size=2 color='gray'>Data Processing Based Python @ <font color='blue'><a href='https://www.facebook.com/jskim.kr'>FB / jskim.kr</a></font>, [김진수](bigpycraft@gmail.com)</font></div>
<hr>

## <font color='brown'>Python Basic </font>
> 
- 표준출력문, print( )
- 표준입력문, input( )
- 주석문, comment

### 문자 출력


```python
# 문자 출력
print('Hello, Python !!')
print('반갑습니다. \n파이썬세계로 온것을 환영합니다.')
print("문자는 반드시 인용부호(\' \' 혹은 \" \")로 감싸야 합니다.")
```

### 숫자 출력


```python
# 숫자 출력
print(100)
print(150 + 200)
print(150 - 200)
```


```python
# 기본연산
x = 50
y = 4.

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
print("x ** y = ", x**y)
print("pow(x,y) = ", pow(x,y))
```

### 변수, Variable


```python
# 변수에 문자담기
name = '홍길동'
greeting = '안녕'

print(name, greeting)
print(greeting, name)

text = name + '님, ' + greeting + '하세요'
print(text)
```


```python
# 변수에 숫자담기
coffee1_name = '카페라떼';  coffee1_val = 4000;
coffee2_name = '카푸치노';  coffee2_val = 4500;
coffee3_name = '마끼야또';  coffee3_val = 5000;
```


```python
# Case 1 
print('손님, ' + coffee1_name + coffee2_name + coffee3_name + '를 주문하셨습니다.')
print('가격은 ' + coffee1_val + coffee2_val + coffee3_val + '원 입니다.')
# TypeError 발생
```


```python
# Case 2
print('손님, ' + coffee1_name + coffee2_name + coffee3_name + '를 주문하셨습니다.')
print('가격은 ' + str(coffee1_val + coffee2_val + coffee3_val) + '원 입니다.')
```


```python
# Case 3
coffee_val = coffee1_val + coffee2_val + coffee3_val
print('손님, \n%s, %s, %s를 주문하셨습니다.' % (coffee1_name, coffee2_name, coffee3_name))
print('가격은 %d원 입니다.' % coffee_val)
```

### 표준 입력 함수


```python
# Case 1
name = input('당신의 이름은 무엇입니까? ')

print(name + '님, 반갑습니다.')
```


```python
# Case 2
order = input('OO카페입니다. \n무엇을 주문하시겠습니까? ')
count = input('몇 잔을 드릴까요? ')

print('%s %s잔을 주문하셨습니다. \n잠시만 기다려주세요~^^' % (order, count))
```


```python
# Case 3
price = 4500
cost  = price * count

print('%s %s잔을 주문하셨습니다. \n결재하실 금액은 %s원입니다~^^' % (order, count, cost))
```


```python
# Case 4
price = 4500
cost  = price * int(count)

print('%s %s잔을 주문하셨습니다. \n결재하실 금액은 %d원입니다~^^' % (order, count, cost))
```

### 주석문
> 
- 한줄 주석 : 샵기호(#)로 시작하는 줄
- 블럭 주석 : 큰따옴표 3개로 감사는 줄


```python
# 이 줄은 라인 코멘트입니다
print ("Hello World!")
print ("Hello World!")    # 이것도 라인 코멘트입니다
print ("Hello World!")    # 이것도 라인 코멘트입니다
```


```python
# First comment
a = 12    # second comment
# a 값을 출력해보세요!

print(a)
b = '파이선의 주석은 샵기호(#)로 시작합니다.'
print(b)
# 마지막 라인입니다.
```


```python
# Comment, 한줄주석과 블럭주석

"""
블럭주석, 
즉 멀티라인의 주석문은 따옴표(''' ''') 3개
"""
# 한줄주석문은 샵(#)기호

pass
```

### Turtle Exam


```python
# 거북이 소개
import turtle
import time

input ('엔터를 치면 거북이를 소개합니다.^^')

turtle.shape('turtle')

print('앞으로 전진합니다.')
time.sleep(1)
turtle.forward(100)

print('한번더 앞으로 전진합니다.')
time.sleep(1)
turtle.forward(100)

print('왼쪽으로 전진합니다.')
time.sleep(1)
turtle.left(90)
turtle.forward(100)

print('오른쪽으로 전진합니다.')
time.sleep(1)
turtle.right(90)
turtle.forward(100)

turtle.done()
```


```python
# 거북이로 다각형 그리기 
import turtle

turtle.pensize(10)

# 사각형 그리기
input('엔터를 치면 사각형을 그립니다.')

turtle.color("red")
turtle.forward(200)

turtle.left(90)
turtle.forward(200)

turtle.left(90)
turtle.forward(200)

turtle.left(90)
turtle.forward(200)

turtle.done()
```


```python
# 삼각형 그리기
input('엔터를 치면 빨간색 삼각형을 그립니다.')

turtle.color("green")

turtle.right(30)
turtle.forward(300)

turtle.left(120)
turtle.forward(300)

turtle.left(120)
turtle.forward(300)

turtle.done()
```


```python
# 원그리기
input('엔터를 치면 파란색 굵은 원을 그립니다.')

turtle.right(30)
turtle.color("blue")
turtle.circle(200)

turtle.done()
```


```python
# 사각형 그리기 응용
import turtle

size  = input('사각형의 크기를 입력하세요.[100~300] ')
color = input('선의 색깔을 입력하세요.[red / green / blue]  ')
thick = input('펜의 굵기를 입력하세요.[1~30]   ')

angle = 90
thick = int(thick)
size  = int(size)

turtle.color(color)
turtle.pensize(thick)

turtle.left(angle)
turtle.forward(size)

turtle.left(angle)
turtle.forward(size)

turtle.left(angle)
turtle.forward(size)

turtle.left(angle)
turtle.forward(size)

turtle.done()
```

<hr>
<marquee><font size=3 color='brown'>The BigpyCraft find the information to design valuable society with Technology & Craft.</font></marquee>
<div align='right'><font size=2 color='gray'> &lt; The End &gt; </font></div>
