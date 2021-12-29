*리스트, 튜플, 딕셔너리, 반복문, 그리고 파이썬 모듈에 대한 문법 정리*



# 1. List

* 정의 : 순서대로 나열된 값들

* data type은 무관

* []속 값들을 Comma로 구분

* 각각의 값에는 index(0,1,2,...)가 부여되고 이를 이용해 읽고 쓸 수 있음


```python
grade_list = ["A+", 97, 2] 
word_list = ["apple"]

print(grade_list[0])
print(grade_list[1])
print(grade_list[2])
print(grade_list)
```
A+
97
2
['A+', 97, 2]



# 2. List 갱신하기 & 추가하기

* 갱신할 때는 인덱스를 활용할 수 있다. index 1번의 값인 "chicken"이 "juice"로 갱신된 것을 확인할 수 있다.

* list.append() 함수를 이용하면 리스트에 새로운 값을 추가할 수 있다.

* 이 때 food_list = food_list.append["truffle"]와 같이 변수를 설정하지 않도록 주의하자.


```python
food_list = ["apple", "chicken", "pizza"] 
food_list[1] = "juice" 

food_list.append("truffle") 

print(food_list)
```
['apple', 'juice', 'pizza', 'truffle']



# 3. split(문자열로부터 리스트 생성하기)




```python
university_names = "yonsei, seoul, korea"
university_list = university_names.split(", ")

print(university_list)
```

    ['yonsei', 'seoul', 'korea']



# 4. Two-Dimensional list(Table)




```python
table_list = [[85,91,89],[78,87,98],[49,57,59]] # list의 값으로 또 다른 list를 가지고 있는 형태
table_list = [[85,91,89],
              [78,87,98],
              [49,57,59]] # 보기 좋게 이렇게 표현하기도 한다.

table_list[0][2] # Two-Dimensional list 또한 각각의 행과 열에 index가 부여된다.
print(table_list[1][1])
```

    87



# 5. Tuple

* Tuple : 순서대로 나열된 값. 

* 리스트와 거의 동일하지만 튜플은 값들을 추가하거나 변경할 수 없다.

* 대괄호 대신 소괄호를 사용한다. 

```python
grade_tuple = (96,98,94)
not_a_tuple = (4.3) # 리스트와 달리 튜플에 하나의 값만 존재하게 된다면 컴퓨터는 튜플이 아닌 실수로 인식한다. 
good_tuple = (4.3,) # 이럴 때는 값 뒤에 comma를 붙여주게 된다.

type(good_tuple)
```


    tuple



# 6. Unpacking a List & Tuple




```python
a, b, c = (10, 20, 30) # 튜플의 각각의 값을 변수 a,b,c에 저장하는 문법이다.
d, e, f = 40, 50, 60 # 언팩킹의 경우 튜플의 소괄호는 생략 가능하다.
h, i, j = ["A+", "B-", "C0"] # 리스트의 각각의 값이 변수 h,i,j에 지정된다.

print(a,b,c,d,e,f,g,h,i,j)
```

    10 20 30 40 50 60 3 A+ B- C0

**중요한 점은 변수의 개수와 list & tuple의 개수가 같아야 Unpacking이 가능하다. **



# 7. Slicing List




```python
original_list = ["I", "love", "you", "3000", "4000", "5000"]
new_list = original_list[2:4] 

print(new_list)
```

    ['you', '3000']

* original_list[a:b]는 a 이상 b 미만까지만 뽑는다는 뜻. 나중에 나올 loc문법과 혼동하지 않도록 주의하자. 

* new_list의 값의 갯수는 abs(b-a)

* original_list에는 변동이 없다.

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



# 7. Dictionary




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



# 8. Dictionary(갱신하기 & 추가하기)




```python
korea_dict["builder"] = "단군" # 추가하기
korea_dict["food"] = "bulgogi" # 갱신하기
# 갱신하기, 추가하기는 똑같은 문법을 사용하지만 
# 키값이 기존의 딕셔너리에 있냐 없냐에 따라 각각 갱신, 추가됨

korea_dict
```


    {'builder': '단군', 'food': 'bulgogi', 'population': 5000, 'war': 1950}



# 9. Column name을 가진 표을 Dictionary로 표현하기(4번과 비교)



실제로는 표를 이러한 방법으로 작성하는 것은 아니고 데이터과학에서 주로 사용하는 DataFrame이라는 구조를 만들기 위한 초기 데이터로 활용된다.


```python
num_dict = {"science" : [67,45,98], 
            "math" : [87,56,97],
            "korean" : [12,67,45]}
# num_dict의 column name은 각각 "science", "math", "korean"이 된다.
# 또한 list안의 값들은 4번과 달리 행의 값이 아닌 열의 값이 된다.

num_dict              
```


    {'korean': [12, 67, 45], 'math': [87, 56, 97], 'science': [67, 45, 98]}



# 10. For loop(반복문)



* for in range(start, stop, step) start : 처음, stop : 끝, step : 증감 간격
* 반복문 뒤에 오는 반복되는 구문은 4칸 들여쓰기!
* Error 1 - SyntaxError: invalid syntax: for 반복문의 형식을 지키지 않았을 때 발생하는 구문. for 반복문의 형식에 맞는지 확인하기. 특히 for 끝에 :(콜론)을 빠뜨리지 않았는지 확인.
* Error 2 - SyntaxError: expected an indented block: for 다음 줄에 오는 반복할 코드의 들여쓰기가 맞지 않아서 발생하는 구문 에러. 반복할 코드에서 들여쓰기 4칸을 했는지 확인.


```python
for r in range(0, 7, 2):

    print(r) 
```

    0
    2
    4
    6

```python
area_list = []

for r in range(1, 33, 3): # 콜론 주의
    area = 3.14 * r ** 2 # 4칸 들여쓰기 주의
    area_list.append(area)

print(area_list)    
```

    [3.14, 50.24, 153.86, 314.0, 530.66, 803.84, 1133.54, 1519.76, 1962.5, 2461.76, 3017.54]



# 11. For loop(반복문) + List & Tuple & Dict




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

```
{'coValue': [0.5, 0.9, 1.2, 1.3, 1.1], 'pm25Value': [10, 12, 15, 21, 19]}
```



# 12. Python Module



* 파이썬 모듈은 변수와 함수 등을 모아 놓은 파일

* 다른 파이썬 파일을 import해 작성된 변수 값과 함수의 기능을 재사용할 수 있음. 


```python
import random # 모듈을 가져오는 방법
from random import randint # 모듈이 가지고 있는 특정 기능만 가져오기
```



# 13. Random Module




```python
from random import randint
dice = randint(1, 6) # randint(a,b) a와 b사이 정수 중 랜덤뽑기 (a,b는 정수이고 a,b 포함한다)

from random import choice
color = choice(["red", "green", "blue"]) # choice([]) []안의 값들 중 하나를 랜덤선택 ([]안에는 정수, 문자열 모두 가능)
num = choice([0,4,8,123])

print(dice, color, num)
```

    3 green 123



# 14. Datetime Module 

* 날짜 & 시간과 관련된 연산을 제공하는 모듈
* 연월일, 날짜, 시간 등의 정보를 추출할 수 있다.
* weekday() 함수는 월요일부터 0 인덱스 값을 부여한다. 소괄호 주의


```python
import datetime

dt = datetime.datetime.now()

print(dt.month, dt.year, dt.day, dt.weekday(), dt.hour) 
```

    10 2021 7 3 8



# 15. About Function



* 함수는 어떤 특정한 작업을 실행하는 코드를 묶어놓은 단위

* 함수는 결과값을 반환하는 경우(abs(), round(), float())와 함수 호출 자체가 실행 결과인 경우(append(), print())가 있다.

* Default argument란 함수에 넘겨주는 인수를 생략할 때(for in range(1,10,생략)) 기본적으로 함수에 넘겨지는 값이다

* Keyword argument란 함수에 인수를 key = value 형식으로 넘겨줄 수 있는 것이다. 

* 예를 들어 round()는 round(number, ndigits)로 key값이 설정되어있다. 따라서 round(number=1/3, ndigits=3)이라고 표현할 경우

* 인수들의 순서를 바꾸어도 무방하며 더욱 직관적으로 이해할 수 있게 된다.



# 16. 연속적인 함수 호출



* 이렇게 다양한 함수들을 "."을 활용해 연속적으로 호출할 수 있다. 


```python
txt = "<Jan,Feb,Mar,Apr>"

modified = text.upper().replace("<","").replace(">","").split(",") # upper() 함수는 모두 대분자로 바꾸는 기능. 

print(modified)
```

    ['JAN', 'FEB', 'MAR', 'APR']

