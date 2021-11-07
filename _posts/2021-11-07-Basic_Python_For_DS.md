데이터 과학을 위한 파이썬 기초

Print()


```python
print() # print 함수는 괄호 안의 값을 출력해주는 기능을 한다. 

print("Hello World")
```

    
    Hello World


Variables


```python
txt = "Hello World" 

# 변수에는 다양한 값을 넣을 수 있다.
# 값은 정수, 실수, 표 등등 많은 것들이 될 수 있다. 
# 변수에 들어갈 값을 지정할 때 등호를 사용한다. 
# 변수의 이름은 알파벳, 숫자, _로만 작성. 단 숫자로 시작할 수 없다. 
# 대소문자를 구분함. 공백 안됨. 파이썬에서 이미 사용되고 있는 명령어(print, in, for...etc)는 변수명으로 사용 불가

print(txt)
```

    Hello World


Data Type


```python
# Python에는 다양한 Data Type이 존재한다.
# 정수(int) : 1, -10, 100, 0...
# 실수(float) : 3.14, 10.0...
# 문자열(str) : "Hello World", "시현"
# 논리값(bool) : True or False, ex) r = 10 > -10, r = True, type(r) = bool

# 자료형이 중요한 이유는 일부 예외를 제외하고 산술 및 논리 연산은 같은 자료형 간에만 가능하다. 
```

arithmetic operation



```python
a = 10 + 10 # 덧셈
b = 10 - 87 # 뺄셈
c = 45 * 495 # 곱셈
d = 123 ** 1 # 거듭제곱
e = 45 / 9 # 나눗셈
f = 45 // 6 # 몫 구하기 
g = 45 % 6 # 나머지 구하기
h = 45 + 7 * (6 ** (5 / 3)) # 대괄호나 중괄호가 아닌 오직 소괄호만을 이용해 연산 순서를 지정한다. 

print(a,b,c,d,e,f,g,h) #print 함수에 변수나 값을 ','로 연결하면 여러개를 한번에 보여줄 수 있다.
```

    20 -77 22275 123 5.0 7 3 183.68094445357434


Round off


```python
a = 13.352332423

round(a, 3) # round 함수는 반올림 기능이 있다. 형태는 round(반올림 대상, 몇번째 자리까지?)
```




    13.352



Absolute value


```python
a = -13.352332423

abs(a) # abs 함수는 절댓값을 표현해주는 기능이다.
```




    13.352332423



Logical operation



```python
a = 10 == 10
b = 10 != 45
c = 34 > 58
d = 35 >= 34
e = 45 <= 23
f = 67 < 12

print(a,b,c,d,e,f)
```

    True True False True False False


Boolean Operators 


```python
B1 = a and b # True and True = True
B2 = a and c # True and False = False
B3 = a or b # True or True = True
B4 = a or c # True or False = True
B5 = not a # not True = False
B6 = not c # not False = Ture

# and(교집합), or(합집합), not(여집합)이라고 생각하면 이해가 쉽다.

print(B1,B2,B3,B4,B5,B6)
```

    True False True True False True


**예제**
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

    False


f-string(서식을 적용한 문자열 생성하기)


```python
age = 20
height = 167
txt1 = f"My age is {age} and my height is {height}" # 형식은 f”…str…{value}…str…”이며 변하지 않는 문자열은 대괄호 밖에 가변값이나 변수는 대괄호에 안에 넣는다.

month = "April"
year = 1885
txt2 = f"{month}, {year}"

print(txt1, txt2)
```

    My age is 20 and my height is 167 April, 1885


f-string에서 반올림하기


```python
pi = 3.141592
txt = f"pi = {pi :.1f}" # 형식은 f”…str…{value}…str…” 대괄호 사이에 value :.1f or value :.2f... 
# 숫자는 반올림자릿수, f는 float
# f-string과 round 함수의 결정적인 차이
# round는 숫자 -> 숫자
# f-string은 숫자 -> 문자열

print(txt)
type(txt)
```

    pi = 3.1





    str



Replace()


```python
txt1 = "Hello World"
txt2 = txt1.replace("Hello", "World") # 형식은 “str”.replace(“원래 값”, “바꿀 값”)


print(txt2)
```

    World World


Change "str" to float or int


```python
# important condition : 문자열이 정수나 실수 형태인 문자열이어야 한다

pi = "3.141592"
pi = float(pi) # float() 함수는 다른 형태의 Data Type을 Float으로 바꿔준다.

length = "170"
length = float(length) # int() 함수는 다른 형태의 Data Type을 Int로 바꿔준다.

result = pi ** length # 같은 유형의 데이터끼리만 연산 가능

print(pi, length, result)
type(length)
```

    3.141592 170.0 3.2768985642701405e+84





    float



문자열에서 부분문자열의 위치 찾기


```python
name = "Allen, Mr. William Henry"
position = name.find("William") # "full_str".find("sub_str") 

print(position)
```

    11


List


```python
grade_list = ["A+", 97, 2] 
word_list = ["apple"]

# 정의 : 순서대로 나열된 값들
# data type은 무관
# []속 값들을 Comma로 구분
# 각각의 값에는 index(0,1,2,...)가 부여되고 이를 이용해 읽고 쓸 수 있음

print(grade_list[0])
print(grade_list[1])
print(grade_list[2])
print(grade_list)
```

    A+
    97
    2
    ['A+', 97, 2]


List 갱신하기 & Value append


```python
food_list = ["apple", "chicken", "pizza"] 
food_list[1] = "juice" # 그냥 바꾸면 된다. index 1번의 값인 "chicken"이 "juice"로 갱신된 것을 확인할 수 있다.

food_list.append("truffle") 
# list.append() 함수를 이용하면 리스트에 새로운 값을 추가할 수 있다.
# 이 때 food_list = food_list.append["truffle"]와 같이 변수를 설정하지 않도록 주의하자.

print(food_list)
```

    ['apple', 'juice', 'pizza', 'truffle']


split(문자열로부터 리스트 생성하기)


```python
university_names = "yonsei, seoul, korea"
university_list = university_names.split(", ")

print(university_list)
```

    ['yonsei', 'seoul', 'korea']


Two-Dimensional list(Table)


```python
table_list = [[85,91,89],[78,87,98],[49,57,59]] # list의 값으로 또 다른 list를 가지고 있는 형태
table_list = [[85,91,89],
              [78,87,98],
              [49,57,59]] # 보기 좋게 이렇게 표현하기도 한다.

table_list[0][2] # Two-Dimensional list 또한 각각의 행과 열에 index가 부여된다.
print(table_list[1][1])
```

    87


Tuple



```python
# Tuple : 순서대로 나열된 값. 
# 리스트와 거의 동일하지만 튜플은 값들을 추가하거나 변경할 수 없다.
# 대괄호 대신 소괄호를 사용한다. 

grade_tuple = (96,98,94)
not_a_tuple = (4.3) # 리스트와 달리 튜플에 하나의 값만 존재하게 된다면 컴퓨터는 튜플이 아닌 실수로 인식한다. 
good_tuple = (4.3,) # 이럴 때는 값 뒤에 comma를 붙여주게 된다.

type(good_tuple)
```




    tuple



Unpacking a List & Tuple


```python
a, b, c = (10, 20, 30) # 튜플의 각각의 값을 변수 a,b,c에 저장하는 문법이다.
d, e, f = 40, 50, 60 # 언팩킹의 경우 튜플의 소괄호는 생략 가능하다.
h, i, j = ["A+", "B-", "C0"] # 리스트의 각각의 값이 변수 h,i,j에 지정된다.

#중요한 점은 변수의 개수와 list & tuple의 개수가 같아야 Unpacking이 가능하다. 

print(a,b,c,d,e,f,g,h,i,j)
```

    10 20 30 40 50 60 3 A+ B- C0


Slicing List


```python
original_list = ["I", "love", "you", "3000", "4000", "5000"]
new_list = original_list[2:4] 
# original_list[a:b]는 a 이상 b 미만까지만 뽑는다는 뜻. 나중에 나올 loc문법과 혼동하지 않도록 주의하자. 
# new_list의 값의 갯수는 |b-a|
# original_list에는 변동이 없다.

print(new_list)
```

    ['you', '3000']



```python
# 대괄호 안의 숫자들은 각각 생략이 가능하고 생략 시 시퀀스의 각각 처음과 끝을 의미

print(original_list[0:])
print(original_list[:4])
print(original_list[-1:]) # 리스트 안의 값들은 앞에서부터 0 뒤에서부터 -1의 두개의 인덱스를 부여받는다.
print(original_list[:-3])
```

    ['I', 'love', 'you', '3000', '4000', '5000']
    ['I', 'love', 'you', '3000']
    ['5000']
    ['I', 'love', 'you']


Dictionary


```python
korea_dict = {"food" : "kimchi", "war" : 1950, "population" : 5000}
# Dictionary는 key값으로 data값에 바로 접근할 수 있는 자료 구조.
# 형태는 대괄호 속 {key1: value1, key2 : value2,...} 처럼 쌍으로 값을 표현하며 Key는 중복X
# 대용량 데이터에서 키 값으로 원하는 데이터를 빠르게 접근할 때 효율적

print(korea_dict["food"]) # key 값을 []속에 넣으면 value 값이 도출됨.
print(korea_dict["war"])
print(korea_dict["population"])
```

    kimchi
    1950
    5000


Dictionary 갱신하기 & 추가히기


```python
korea_dict["builder"] = "단군" # 추가하기
korea_dict["food"] = "bulgogi" # 갱신하기
# 갱신하기, 추가하기는 똑같은 문법을 사용하지만 
# 키값이 기존의 딕셔너리에 있냐 없냐에 따라 각각 갱신, 추가됨

korea_dict
```




    {'builder': '단군', 'food': 'bulgogi', 'population': 5000, 'war': 1950}



Column name을 가진 표을 Dictionary로 표현하기
(17.과 비교)

실제로는 표를 이러한 방법으로 작성하는 것은 아니고 데이터과학에서 주로 사용하는 DataFrame이라는 구조를 만들기 위한 초기 데이터로 활용된다.


```python
num_dict = {"science" : [67,45,98], 
            "math" : [87,56,97],
            "korean" : [12,67,45]}
# num_dict의 column name은 각각 "science", "math", "korean"이 된다.
# 또한 list안의 값들은 17번과 달리 행의 값이 아닌 열의 값이 된다.

num_dict              
```




    {'korean': [12, 67, 45], 'math': [87, 56, 97], 'science': [67, 45, 98]}



For loop(반복문)


```python
for r in range(0, 7, 2): # for in range(start, stop, step) start : 처음, stop : 끝, step : 증감 간격

    print(r) 
# 반복문 뒤에 오는 반복되는 구문은 4칸 들여쓰기!
# Error 1 - SyntaxError: invalid syntax: for 반복문의 형식을 지키지 않았을 때 발생하는 구문. for 반복문의 형식에 맞는지 확인하기. 특히 for 끝에 :(콜론)을 빠뜨리지 않았는지 확인.
# Error 2 - SyntaxError: expected an indented block: for 다음 줄에 오는 반복할 코드의 들여쓰기가 맞지 않아서 발생하는 구문 에러. 반복할 코드에서 들여쓰기 4칸을 했는지 확인.
```

    0
    2
    4
    6



```python
area_list = []

for r in range(1, 33, 3): # 콜론 주의
    area = 3.14 * r ** 2 # 들여쓰기 주의
    area_list.append(area)

print(area_list)    
```

    [3.14, 50.24, 153.86, 314.0, 530.66, 803.84, 1133.54, 1519.76, 1962.5, 2461.76, 3017.54]


For loop(반복문) + List & Tuple & Dict


```python
Delicious = ["떡볶이", "차돌박이", "비빔면"] # 각각의 값들이 순차적으로 D 변수에 대입된다.
Animal = ("lion", "tiger", "zebra") # 각각의 값들이 순차적으로 A 변수에 대입된다.
Company = {"car" : "kia", "cloth" : "gucci"} # Dictionary는 key값이 도출된다.

#for D in Delicious:
#for A in Animal:
for C in Company:
    #print(D)
    #print(A)
    print(C)
```

    car
    cloth


**lab01**

* 주어진 data_dict에서 "pm10Value" 키의 값을 순서대로 리스트로 작성합니다. data_dict의 기본 구조는 변경되지 않지만 "items" 키의 리스트가 가진 딕셔너리의 개수는 가변적입니다.


```python
data_dict = {'response': {'body': {'items': [
{'coValue': 0.5,'pm10Value': 20,'pm25Value': 10}, # 20이 리스트의 첫 번째 값이 된다
{'coValue': 0.9, 'pm10Value': 32, 'pm25Value': 12}, # 32가 리스트의 두 번째 값이 된다
{'coValue': 1.2, 'pm10Value': 45, 'pm25Value': 15}, # 45가 리스트의 세 번째 값이 된다
# {'coValue': 1.4, 'pm10Value': 50, 'pm25Value': 21} # 리스트 안의 딕셔너리는 추가될 수 있다.
# {'coValue': 1.1, 'pm10Value': 47, 'pm25Value': 19} # 리스트 안의 딕셔너리는 추가될 수 있다.
# ..
]
}}}
```


```python
pm10Value_list = []

#for num in range(0,3):
    #data = data_dict["response"]["body"]["items"][num]["pm10Value"]
    #pm10Value_list.append(data)
# or
for data in data_dict["response"]["body"]["items"]:
    pm10Value_list.append(data["pm10Value"])


pm10Value_list
```




    [20, 32, 45]



**lab02**
* 주어진 data_dict를 이용하여 새로운 구조의 table_dict 딕셔너리를 생성합니다.
* table_dict의 key는 header 리스트의 값입니다.
* table_dict의 value는 data_dict에서 header 리스트의 값에 해당하는 값들을 순서대로 나열한 리스트입니다.
* 추가: 난이도를 고려하여 header 리스트를 쓰지 않아도 되는 것으로 하겠습니다. table_dict는 항상 "coValue"와 "pm25Value"를 키 키 값으로 가집니다. 물론 원래대로 header 변수를 사용해도 됩니다.


```python
header = ["coValue", "pm25Value"]
data_dict = {'response': {'body': {'items': [
  {'coValue': 0.5,'pm10Value': 20,'pm25Value': 10},  # {"coValue":[0.5], "pm25Value":[10]} 이 된다.
  {'coValue': 0.9, 'pm10Value': 32, 'pm25Value': 12}, # {"coValue":[0.5, 0.9], "pm25Value":[10, 12]} 이 된다.
  {'coValue': 1.2, 'pm10Value': 45, 'pm25Value': 15}, # {"coValue":[0.5, 0.9, 1.2], "pm25Value":[10, 12, 15]} 이 된다.
  {'coValue': 1.3, 'pm10Value': 50, 'pm25Value': 21}, # 이하 동일. header의 값에 따라 딕셔너리의 키는 달라진다.
  {'coValue': 1.1, 'pm10Value': 47, 'pm25Value': 19},
  # {'coValue': 0.8, 'pm10Value': 39, 'pm25Value': 17}, # 리스트 안의 딕셔너리는 추가될 수 있다.
  # {'coValue': 1.0, 'pm10Value': 20, 'pm25Value': 22}, # 리스트 안의 딕셔너리는 추가될 수 있다.
  ]
  }}}
```


```python
coValue_list = []
pm25Value_list = []

for data in data_dict["response"]["body"]["items"]:
    coValue_list.append(data["coValue"])
    pm25Value_list.append(data["pm25Value"])

table_dict = {"coValue" : coValue_list, "pm25Value" : pm25Value_list}

print(table_dict)
```

    {'coValue': [0.5, 0.9, 1.2, 1.3, 1.1], 'pm25Value': [10, 12, 15, 21, 19]}


Python Module


```python
# 파이썬 모듈은 변수와 함수 등을 모아 놓은 파일
# 다른 파이썬 파일을 import해 작성된 변수 값과 함수의 기능을 재사용할 수 있음. 

import random # 모듈을 가져오는 방법
from random import randint # 모듈이 가지고 있는 특정 기능만 가져오기
```

Random Module


```python
from random import randint
dice = randint(1, 6) # randint(a,b) a와 b사이 정수 중 랜덤뽑기 (a,b는 정수이고 a,b 포함한다)

from random import choice
color = choice(["red", "green", "blue"]) # choice([]) []안의 값들 중 하나를 랜덤선택 ([]안에는 정수, 문자열 모두 가능)
num = choice([0,4,8,123])

print(dice, color, num)
```

    3 green 123


Datetime Module 


```python
# 날짜 & 시간과 관련된 연산을 제공하는 모듈

import datetime

dt = datetime.datetime.now()

print(dt.month, dt.year, dt.day, dt.weekday(), dt.hour) 
# 연월일, 날짜, 시간 등의 정보를 추출할 수 있다.
# weekday() 함수는 월요일부터 0 인덱스 값을 부여한다. 소괄호 주의
```

    10 2021 7 3 8


About Function


```python
# 함수는 어떤 특정한 작업을 실행하는 코드를 묶어놓은 단위
# 함수는 결과값을 반환하는 경우(abs(), round(), float())와 함수 호출 자체가 실행 결과인 경우(append(), print())가 있다.
# Default argument란 함수에 넘겨주는 인수를 생략할 때(for in range(1,10,생략)) 기본적으로 함수에 넘겨지는 값이다
# Keyword argument란 함수에 인수를 key = value 형식으로 넘겨줄 수 있는 것이다. 
# 예를 들어 round()는 round(number, ndigits)로 key값이 설정되어있다. 따라서 round(number=1/3, ndigits=3)이라고 표현할 경우
# 인수들의 순서를 바꾸어도 무방하며 더욱 직관적으로 이해할 수 있게 된다.
```

연속적인 함수 호출


```python
txt = "<Jan,Feb,Mar,Apr>"

modified = text.upper().replace("<","").replace(">","").split(",") # upper() 함수는 모두 대분자로 바꾸는 기능. 
# 이렇게 다양한 함수들을 "."을 활용해 연속적으로 호출할 수 있다. 

print(modified)
```

    ['JAN', 'FEB', 'MAR', 'APR']

