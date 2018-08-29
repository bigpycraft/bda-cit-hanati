
<center>
<b><font size=6>Industry 4.0 의 중심, BigData</font></b>
</center>

<div align='right'><font size=2 color='gray'>Data Processing Based Python @ <font color='blue'><a href='https://www.facebook.com/jskim.kr'>FB / jskim.kr</a></font>, 김진수</font></div>
<hr>

## <font color='brown'>데이터구조, Data Structure</font>
> 
- 리스트형, List Type
- 튜플형, Tuple Type
- 세트형, Set Type
- 사전형, Dictionary Type

### 리스트형, List

#### 리스트형 선언 및 색인


```python
# 리스트형 선언 및 색인
bts_members = ['RM', '슈가', '진', '제이홉', '지민', '뷔', '정국']

# 변수의 타입 확인
print('멤버 :', bts_members)
print('타입 :', type(bts_members))
print('크기 :', len(bts_members))
```

    멤버 : ['RM', '슈가', '진', '제이홉', '지민', '뷔', '정국']
    타입 : <class 'list'>
    크기 : 7
    


```python
print('리스트멤버 호출')
print(bts_members[0])
print(bts_members[1])
print(bts_members[2])
print(bts_members[3])
```

    리스트멤버 호출
    RM
    슈가
    진
    제이홉
    


```python
print('리스트멤버 호출(역순)')
print(bts_members[-1])
print(bts_members[-2])
print(bts_members[-3])
print(bts_members[-4])
```

    리스트멤버 호출(역순)
    정국
    뷔
    지민
    제이홉
    

#### 리스트형 추가/삭제


```python
# 리스트형 추가/삭제
sistar_members = ['효린', '소유']
print('씨스타 \t:', sistar_members)

sistar_members.append('다솜')
print('append \t:', sistar_members)
sistar_members.insert(1, '보라')
print('insert \t:', sistar_members)

sistar_members.remove('소유')
print('remove \t:', sistar_members)

pickup = sistar_members.pop(0)
print('pop   \t:', sistar_members, end=' ---> ')
print(pickup)

```

    씨스타 	: ['효린', '소유']
    append 	: ['효린', '소유', '다솜']
    insert 	: ['효린', '보라', '소유', '다솜']
    remove 	: ['효린', '보라', '다솜']
    pop   	: ['보라', '다솜'] ---> 효린
    

#### 리스트 슬라이싱


```python
# 리스트 슬라이싱
rainbow = ['빨강', '주황', '노랑', '초록', '파랑', '남색', '보라']
print('\n무지개색깔 \t :', rainbow)

result = rainbow[2:5]
print('rainbow[2:5] :', result)

result = rainbow[:3]
print('rainbow[ :3] :', result)

result = rainbow[:]
print('rainbow[ : ] :', result)

result = rainbow[::2]
print('rainbow[::2] :', result)

result = rainbow[-3:]
print('rainbow[-3:] :', result)

result = rainbow[::-1]
print('rainbow[::-1]:', result)

```

    
    무지개색깔 	 : ['빨강', '주황', '노랑', '초록', '파랑', '남색', '보라']
    rainbow[2:5] : ['노랑', '초록', '파랑']
    rainbow[ :3] : ['빨강', '주황', '노랑']
    rainbow[ : ] : ['빨강', '주황', '노랑', '초록', '파랑', '남색', '보라']
    rainbow[::2] : ['빨강', '노랑', '파랑', '보라']
    rainbow[-3:] : ['파랑', '남색', '보라']
    rainbow[::-1]: ['보라', '남색', '파랑', '초록', '노랑', '주황', '빨강']
    

#### 리스트 인덱싱


```python
solarsys = ['태양', '수성', '금성', '지구', '화성', '목성', '토성', '천왕성', '해왕성', '지구']
print('태양계 :', solarsys)

# 리스트에서 특정 요소의 위치 구하기(index)
planet = '지구'
pos = solarsys.index(planet)
print('%s 행성은 태양계에서 %d번째에 위치하고 있습니다.' %(planet, pos))
pos = solarsys.index(planet, 5)
print('%s 행성은 태양계에서 %d번째에 위치하고 있습니다.' %(planet, pos))

# 리스트에서 특정 위치의 요소를 변경하기
solarsys.pop(-1)
print('태양계 :', solarsys)

planet = '화성'
pos = solarsys.index(planet)
solarsys [pos] = 'Mars'
print('태양계 :', solarsys)

# 리스트에서 특정 구간에 있는 요소 추출하기
solarsys = ['태양', '수성', '금성', '지구', '화성', '목성', '토성', '천왕성', '해왕성']
rock_planets = solarsys[1:5]
gas_planets  = solarsys[5: ]

print('암석형 행성: ', end=''); print(rock_planets);
print('가스형 행성: ', end=''); print(gas_planets);

# 리스트의 특정 위치에 요소 삽입하기(insert)
solarsys = ['태양', '수성', '금성', '지구', '화성', '목성', '토성', '천왕성', '해왕성']
pos = solarsys.index('목성')
solarsys.insert(pos, '소행성')
print('태양계 :', solarsys)

```

#### 중첩리스트


```python
#3x3 2차원 행렬을 중첩리스트로 선언
city = [
    ['서울',  '도쿄',  '베이징'],
    ['런던',  '파리',  '로마'  ],
    ['워싱턴','시카고','잭슨빌']
]

print('city      :', city)
print('city[0]   :', city[0])
print('city[1]   :', city[1])
print('city[-1]  :', city[-1])
print('city[0][0]:', city[0][0])
print('city[0][1]:', city[0][1])
print('city[0][2]:', city[0][2])
print('city[1][1]:', city[1][1])
print('city[2][0]:', city[2][0])
```

    city      : [['서울', '도쿄', '베이징'], ['런던', '파리', '로마'], ['워싱턴', '시카고', '잭슨빌']]
    city[0]   : ['서울', '도쿄', '베이징']
    city[1]   : ['런던', '파리', '로마']
    city[-1]  : ['워싱턴', '시카고', '잭슨빌']
    city[0][0]: 서울
    city[0][1]: 도쿄
    city[0][2]: 베이징
    city[1][1]: 파리
    city[2][0]: 워싱턴
    

<hr>
<marquee><font size=3 color='brown'>The BigpyCraft find the information to design valuable society with Technology & Craft.</font></marquee>
<div align='right'><font size=2 color='gray'> &lt; The End &gt; </font></div>
