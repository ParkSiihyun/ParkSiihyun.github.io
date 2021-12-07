---
layout: post
title:  "데이터 과학을 위한 파이썬 기초 1"
---

print, type, find, replace, f"string" 등 정말 기초적인 파이썬 기본 문법 정리

# 1. Print()


```python
print() # print 함수는 괄호 안의 값을 출력해주는 기능을 한다. 

print("Hello World")
```
```
Hello World
```




# 2. Variables


```python
txt = "Hello World" 
print(txt)
```
```
Hello World
```



* 변수에는 다양한 값을 넣을 수 있다.
* 값은 정수, 실수, 표 등등 많은 것들이 될 수 있다. 
* 변수에 들어갈 값을 지정할 때 등호를 사용한다. 
* 변수의 이름은 알파벳, 숫자, _로만 작성. 단 숫자로 시작할 수 없다. 
* 대소문자를 구분함. 공백 안됨. 파이썬에서 이미 사용되고 있는 명령어(print, in, for...etc)는 변수명으로 사용 불가




# 3. Data Type

**자료형이 중요한 이유는 일부 예외를 제외하고 산술 및 논리 연산은 같은 자료형 간에만 가능하기 때문이다.**

* Python에는 다양한 Data Type이 존재한다.
* 정수(int) : 1, -10, 100, 0...
* 실수(float) : 3.14, 10.0...
* 문자열(str) : "Hello World", "시현"
* 논리값(bool) : True or False, ex) r = 10 > -10, r = True, type(r) = bool




# 4. arithmetic operation


```python
a = 10 + 10 # 덧셈
b = 10 - 87 # 뺄셈
c = 45 * 495 # 곱셈
d = 123 ** 1 # 거듭제곱
e = 45 / 9 # 나눗셈
f = 45 // 6 # 몫 구하기 
g = 45 % 6 # 나머지 구하기
h = 45 + 7 * (6 ** (5 / 3)) 

print(a,b,c,d,e,f,g,h) 
```
```
20 -77 22275 123 5.0 7 3 183.68094445357434
```

* **대괄호나 중괄호가 아닌 오직 소괄호만을 이용해 연산 순서를 지정한다.**

* **print 함수에 변수나 값을 ','로 연결하면 여러개를 한번에 보여줄 수 있다.**




# 5. Round off


```python
a = 13.352332423

round(a, 3) 
```
```
13.352
```

* **round 함수는 반올림 기능이 있다. 형태는 round(반올림 대상, 몇번째 자리까지?)**




# 6. Absolute value


```python
a = -13.352332423

abs(a)
```
```
13.352332423
```

* **abs 함수는 절댓값을 표현해주는 기능이다.**




# 7. Logical operation


```python
a = 10 == 10
b = 10 != 45
c = 34 > 58
d = 35 >= 34
e = 45 <= 23
f = 67 < 12

print(a,b,c,d,e,f)
```
```
True True False True False False
```




# 8. abs 함수는 절댓값을 표현해주는 기능이다.Boolean Operators 


```python
B1 = a and b # True and True = True
B2 = a and c # True and False = False
B3 = a or b # True or True = True
B4 = a or c # True or False = True
B5 = not a # not True = False
B6 = not c # not False = Ture

print(B1,B2,B3,B4,B5,B6)
```
```
True False True True False True
```

* **and(교집합), or(합집합), not(여집합)이라고 생각하면 이해가 쉽다.**



**lab01**
*Problem*

* 주어진 타이타닉호 승객의 정보(passenger)에 따라 생존 여부(survived)를 True 혹은 False를  계산하는 식을 작성하세요.
* 여성이면 생존(True)
* 남성이면서 나이가 10살 미만이고 형제자매가 2명 이하이면 생존(True)
* 그 외의 경우는 사망(False)
* 이름(성)에 Mrs.나 Miss.가 붙으면 여성이며 그 외의 경우는 남성으로 계산한다.

Environment Setup

* passenger_list의 값은 승객의 ["이름", 나이, 형제자매의수] 데이터입니다.


```python
passenger_list = [["Allen, Mr. William Henry", 9, 3], 
                  ["McGowan, Miss. Anna Annie", 1, 3], 
                  ["Panula, Mr. Jaako Arnold", 14, 4], 
                  ["Coutts, Master. Eden Leslie", 9, 1]]

passenger = passenger_list[0]
```


```python
cond1 = passenger[0].find("Miss.") != -1 or passenger[0].find("Mrs.") != -1 # 여자인 조건
cond2 = passenger[1] < 10 and passenger[2] <= 2 # 나이가 10살 미만이고 형제자매가 2명인 조건
cond3 = not cond1 # 남성인 조건

Survived = cond1 or cond2 and cond3

print(Survived)
```
```
False
```




# 9. f-string(서식을 적용한 문자열 생성하기)


```python
age = 20
height = 167
txt1 = f"My age is {age} and my height is {height}" 

month = "April"
year = 1885
txt2 = f"{month}, {year}"

print(txt1, txt2)
```
```
My age is 20 and my height is 167 April, 1885
```

* **형식은 f”…str…{value}…str…”이며 변하지 않는 문자열은 대괄호 밖에 가변값이나 변수는 대괄호에 안에 넣는다.**




# 10. f-string에서 반올림하기


```python
pi = 3.141592
txt = f"pi = {pi :.1f}" # 형식은 f”…str…{value}…str…” 대괄호 사이에 value :.1f or value :.2f... 

print(txt)
type(txt)
```
```
pi = 3.1
str
```

* 숫자는 반올림자릿수, f는 float(type)
* f-string과 round 함수의 결정적인 차이
* round는 숫자 -> 숫자
* f-string은 숫자 -> 문자열




# 11. Replace()


```python
txt1 = "Hello World"
txt2 = txt1.replace("Hello", "World") 


print(txt2)
```
```
World World
```

* **형식은 .replace(“원래 값”, “바꿀 값”)**




# 12. Change "str" to float or int


```python
pi = "3.141592"
pi = float(pi) 

length = "170"
length = float(length) 

result = pi ** length 

print(pi, length, result)
type(length)
```
```
3.141592 170.0 3.2768985642701405e+84
float
```

* **important condition : 문자열이 정수나 실수 형태인 문자열이어야 한다.**

* **float() 함수는 다른 형태의 Data Type을 실수로 바꿔준다.**

* **int() 함수는 다른 형태의 Data Type을 정수로 바꿔준다.**

* **같은 유형의 데이터끼리만 연산 가능**




# 13. 문자열에서 부분문자열의 위치 찾기


```python
name = "Allen, Mr.William Henry"
position = name.find("William")

print(position)
```
```
10
```

* **단어의 경우 단어 시작점의 위치를 알려줌**

* **"full_str".find("sub_str")**
