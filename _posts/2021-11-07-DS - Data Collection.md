

## What is Data Science? 

* 데이터를 분석하여 문제 해결에 필요한 지식을 얻는 과학적 방법론을 말한다. 
* 정형 데이터, 비정형 데이터에서 지식이나 통찰력을 추출하기 위해 과학적 방법, 과정, 알고리즘, 시스템을 사용하는 학문이다.
* 데이터 과학의 Process
  * Business Understanding - 문제 정의
  * Data Collection - 데이터 수집
  * Data preparation - 수집된 데이터를 확인 및 기본적인 정보 이해
  * Data Exploration - 데이터 관찰, 이해, 시각화
  * Modeling - 머신러닝 알고리즘을 이용해 예측 혹은 분류 모델을 생성
  * Deployment - 배포




## 1. Data Collection

* 데이터는 어디서 수집할 수 있을까? 
  * Web scraping(html)
  * Open API(json,xml) 
  * 공공데이터포탈
  * kaggle.com(csv,xlsx), etc...




## 2. HTML(Hyper Text Markup Language)

* 태그(tag)를 이용하여 제목<h1>, 본문, 문단<p>등의 문서 구조를 표현하는 방법

* HTML은 웹브라우저에서 Text들이 어떻게 보일 것인가를 결정하는 것.

* ex) <p>This is a paragraph!</p> - This is a paragraph!라는 텍스트가 <p>tag로 묶여 문단으로 보여지게 끔한다.

* HTML과 Browser의 관계 - 웹 브라우저는 HTML 문서(tag)를 해석하여 화면에 텍스트, 이미지, 동영상 등을 출력



## 3. urllib

* urllib : url 처리를 위해 필요한 모듈을 모아놓은 패키지 


```python
import urllib.request
url = "http://www.kma.go.kr/wid/queryDFSRSS.jsp?zone=1141058500"

html = urllib.request.urlopen(url).read().decode()
```

* urllib.request - url을 열고 데이터를 읽기 위한 모듈

  * urlopen() : url을 열고

  * read() : 웹페이지를 읽고

  * decode() : 해독해라



## 4. BeautifulSoup Module(Processing HTML Documents)

* 파이썬의 기본 기능 이용해 HTML을 처리할 수 있지만 굉장히 복잡하다
* BeautifulSoup Module을 이용하면 쉽고 간단하게 HTML 문서를 처리할 수 있다.


```python
from bs4 import BeautifulSoup # BeautifulSoup Module을 불러오는 방법
soup = BeautifulSoup(html, "html.parser") 

print(soup)
```

* html이라는 재료와 "html.parser"라는 도구(파이썬 기본 모듈)를 이용해 BeautifulSoup 요리!
* parse - 분석하다

    <?xml version="1.0" encoding="UTF-8" ?>
    <rss version="2.0">
    <channel>
    <title>기상청 동네예보 웹서비스 - 서울특별시 서대문구 신촌동 도표예보</title>
    <link/>http://www.kma.go.kr/weather/main.jsp
    <description>동네예보 웹서비스</description>
    <language>ko</language>
    <generator>동네예보</generator>
    <pubdate>2021년 10월 15일 (금)요일 17:00</pubdate>
    <item>
    <author>기상청</author>
    <category>서울특별시 서대문구 신촌동</category>
    <title>동네예보(도표) : 서울특별시 서대문구 신촌동 [X=59,Y=126]</title><link/>http://www.kma.go.kr/weather/forecast/timeseries.jsp?searchType=INTEREST&amp;dongCode=1141058500
    <guid>http://www.kma.go.kr/weather/forecast/timeseries.jsp?searchType=INTEREST&amp;dongCode=1141058500</guid>
    <description>
    <header>
    <tm>202110151700</tm>
    <ts>5</ts>
    <x>59</x>
    <y>126</y>
    </header>
    <body>
    <data seq="0">
    <hour>21</hour>
    <day>0</day>
    <temp>19.0</temp>
    <tmx>-999.0</tmx>
    <tmn>-999.0</tmn>
    <sky>4</sky>
    <pty>0</pty>
    <wfkor>흐림</wfkor>
    <wfen>Cloudy</wfen>
    <pop>30</pop>
    <r12>0.0</r12>
    <s12>0.0</s12>
    <ws>1.4000000000000001</ws>
    <wd>1</wd>
    <wdkor>북동</wdkor>
    <wden>NE</wden>
    <reh>75</reh>
    <r06>0.0</r06>
    <s06>0.0</s06>
    </data>
    <data seq="1">
    <hour>24</hour>
    <day>0</day>
    <temp>18.0</temp>
    <tmx>-999.0</tmx>
    <tmn>-999.0</tmn>
    <sky>4</sky>
    <pty>0</pty>
    <wfkor>흐림</wfkor>
    <wfen>Cloudy</wfen>
    <pop>30</pop>
    <r12>0.0</r12>
    <s12>0.0</s12>
    <ws>0.5</ws>
    <wd>2</wd>
    <wdkor>동</wdkor>
    <wden>E</wden>
    <reh>80</reh>
    <r06>0.0</r06>
    <s06>0.0</s06>
    </data>
    <data seq="2">
    <hour>3</hour>
    <day>1</day>
    <temp>17.0</temp>
    <tmx>12.0</tmx>
    <tmn>12.0</tmn>
    <sky>4</sky>
    <pty>0</pty>
    <wfkor>흐림</wfkor>
    <wfen>Cloudy</wfen>
    <pop>30</pop>
    <r12>0.0</r12>
    <s12>0.0</s12>
    <ws>0.9</ws>
    <wd>7</wd>

* soup 객체는 html과 차이가 없어보이지만 html 데이터가 soup 객체가 되면 보이지는 않지만 계층화 된 자료가 된다.



## 5. BeautifulSoup의 기능


```python
p_list = soup.find_all("hour")

for tag in p_list:
    print(tag.get_text())
print(p_list)
```

* soup.find_all("tag_name") 함수는 "tag_name"에 대당되는 모든 tag들을 list로 반환해준다.
* get_text() 함수는 tag객체에서 tag를 제외한 text만을 추출한다.

    21
    24
    3
    6
    9
    12
    15
    18
    21
    24
    3
    6
    9
    12
    15
    18
    21
    24
    [<hour>21</hour>, <hour>24</hour>, <hour>3</hour>, <hour>6</hour>, <hour>9</hour>, <hour>12</hour>, <hour>15</hour>, <hour>18</hour>, <hour>21</hour>, <hour>24</hour>, <hour>3</hour>, <hour>6</hour>, <hour>9</hour>, <hour>12</hour>, <hour>15</hour>, <hour>18</hour>, <hour>21</hour>, <hour>24</hour>]



## 6. Open API(Open Application Programming Interface)

* Open API란 어플리케이션의 기능을 누구나 사용할 수 있도록 공개한 프로그래밍 인터페이스
* ex) 카카오톡 메세지 보내기 API, 파파고 번역 API
* 사용법은 제공하는 주체에 따라 다르지만 최근에는 url에 패러미터 값을 전달하고 응답값을 반환받는 형식이 많이 사용되고 있다.
  * API를 제공하는 사이트에 접속하면 Open API의 URL과 URL뒤에 사용되는 패러미터들이 나온다. 
  * 각 패러미터(기상청의 경우 지역, 날짜, 미세먼지, 초미세먼지 등이 있을 것이다)들은 &로 연결된다. 
  * 각 패러미터에 내가 원하는 값을 넣는다면 내가 원하는 정보를 불러올 수 있다. 

* 웹사이트의 기능들을 손으로 클릭해서 불러올 수 도 있지만 이렇게 Open API를 이용할 수도 있다. 



# 7. XML

* 형식은 HTML과 동일하고 .get_text()나 .find_all()과 같은 함수도 사용가능하다.
* 하지만 XML의 tag는 웹브라우저에 나타내기 위해 사용된 것이 아니기 때문에 사용자가 임의로 지정할 수 있고 이 태그는 웹브라우저에 그대로 나타난다. 
* 주로 실제로 tag안의 값이 갖는 의미를 tag로 쓰는 경우가 많다.
* ex) <my_weight>67</my_weight>

**lab01**


```python
url = 'http://swclass.yonsei.ac.kr:2020/dev/gen/shinchon_dust.xml'
print(url)
```

    http://swclass.yonsei.ac.kr:2020/dev/gen/shinchon_dust.xml



```python
html = urllib.request.urlopen(url)
soup = BeautifulSoup(html, "xml")

soup
```




    <?xml version="1.0" encoding="utf-8"?>
    <response>
    <header>
    <resultCode>00</resultCode>
    <resultMsg>NORMAL_CODE</resultMsg>
    </header>
    <body>
    <items>
    <item>
    <so2Grade>1</so2Grade>
    <coFlag/>
    <khaiValue>47</khaiValue>
    <so2Value>0.002</so2Value>
    <coValue>0.3</coValue>
    <pm25Flag/>
    <pm10Flag/>
    <pm10Value>3</pm10Value>
    <o3Grade>1</o3Grade>
    <khaiGrade>1</khaiGrade>
    <pm25Value>1</pm25Value>
    <no2Flag/>
    <no2Grade>1</no2Grade>
    <o3Flag/>
    <pm25Grade>1</pm25Grade>
    <so2Flag/>
    <dataTime>2021-09-27 06:00</dataTime>
    <coGrade>1</coGrade>
    <no2Value>0.009</no2Value>
    <pm10Grade>1</pm10Grade>
    <o3Value>0.028</o3Value>
    </item>
    <item>
    <so2Grade>1</so2Grade>
    <coFlag/>
    <khaiValue>48</khaiValue>
    <so2Value>0.002</so2Value>
    <coValue>0.3</coValue>
    <pm25Flag/>
    <pm10Flag/>
    <pm10Value>4</pm10Value>
    <o3Grade>1</o3Grade>
    <khaiGrade>1</khaiGrade>
    <pm25Value>2</pm25Value>
    <no2Flag/>
    <no2Grade>1</no2Grade>
    <o3Flag/>
    <pm25Grade>1</pm25Grade>
    <so2Flag/>
    <dataTime>2021-09-27 05:00</dataTime>
    <coGrade>1</coGrade>
    <no2Value>0.007</no2Value>
    <pm10Grade>1</pm10Grade>
    <o3Value>0.029</o3Value>
    </item>
    <item>
    <so2Grade>1</so2Grade>
    <coFlag/>
    <khaiValue>50</khaiValue>
    <so2Value>0.003</so2Value>
    <coValue>0.3</coValue>
    <pm25Flag/>
    <pm10Flag/>
    <pm10Value>3</pm10Value>
    <o3Grade>1</o3Grade>
    <khaiGrade>1</khaiGrade>
    <pm25Value>1</pm25Value>
    <no2Flag/>
    <no2Grade>1</no2Grade>
    <o3Flag/>
    <pm25Grade>1</pm25Grade>
    <so2Flag/>
    <dataTime>2021-09-27 04:00</dataTime>
    <coGrade>1</coGrade>
    <no2Value>0.007</no2Value>
    <pm10Grade>1</pm10Grade>
    <o3Value>0.030</o3Value>
    </item>
    <item>
    <so2Grade>1</so2Grade>
    <coFlag/>
    <khaiValue>51</khaiValue>
    <so2Value>0.002</so2Value>
    <coValue>0.3</coValue>
    <pm25Flag/>
    <pm10Flag/>
    <pm10Value>5</pm10Value>
    <o3Grade>2</o3Grade>
    <khaiGrade>2</khaiGrade>
    <pm25Value>2</pm25Value>
    <no2Flag/>
    <no2Grade>1</no2Grade>
    <o3Flag/>
    <pm25Grade>1</pm25Grade>
    <so2Flag/>
    <dataTime>2021-09-27 03:00</dataTime>
    <coGrade>1</coGrade>
    <no2Value>0.005</no2Value>
    <pm10Grade>1</pm10Grade>
    <o3Value>0.031</o3Value>
    </item>
    <item>
    <so2Grade>1</so2Grade>
    <coFlag/>
    <khaiValue>51</khaiValue>
    <so2Value>0.003</so2Value>
    <coValue>0.3</coValue>
    <pm25Flag/>
    <pm10Flag/>
    <pm10Value>3</pm10Value>
    <o3Grade>2</o3Grade>
    <khaiGrade>2</khaiGrade>
    <pm25Value>1</pm25Value>
    <no2Flag/>
    <no2Grade>1</no2Grade>
    <o3Flag/>
    <pm25Grade>1</pm25Grade>
    <so2Flag/>
    <dataTime>2021-09-27 02:00</dataTime>
    <coGrade>1</coGrade>
    <no2Value>0.006</no2Value>
    <pm10Grade>1</pm10Grade>
    <o3Value>0.031</o3Value>
    </item>
    </items>
    <numOfRows>5</numOfRows>
    <pageNo>1</pageNo>
    <totalCount>23</totalCount>
    </body>
    </response>




```python
pm10Value_list = []
data1 = soup.find_all("pm10Value")
for data2 in data1:
    pm10Value_list.append(data2.get_text())

pm10Value_list
```




    ['3', '4', '3', '5', '3']



1-7. JSON(JavaScript Object Notation)

* key와 value 쌍으로 데이터를 표기하는 방법 { "name" : "gildong", "age": 21 }
* 형식은 딕셔너리와 똑같지만 일정한 형식을을 가진 단순한 텍스트일 뿐이다.

**lab01**


```python
import json

url = 'http://swclass.yonsei.ac.kr:2020/dev/gen/shinchon_dust.json'
print(url)
```

    http://swclass.yonsei.ac.kr:2020/dev/gen/shinchon_dust.json



```python
html = urllib.request.urlopen(url).read().decode()
raw_dict = json.loads(html)

raw_dict
```




    {'response': {'body': {'items': [{'coFlag': None,
         'coGrade': '1',
         'coValue': '0.3',
         'dataTime': '2021-09-27 06:00',
         'khaiGrade': '1',
         'khaiValue': '47',
         'no2Flag': None,
         'no2Grade': '1',
         'no2Value': '0.009',
         'o3Flag': None,
         'o3Grade': '1',
         'o3Value': '0.028',
         'pm10Flag': None,
         'pm10Grade': '1',
         'pm10Value': '3',
         'pm25Flag': None,
         'pm25Grade': '1',
         'pm25Value': '1',
         'so2Flag': None,
         'so2Grade': '1',
         'so2Value': '0.002'},
        {'coFlag': None,
         'coGrade': '1',
         'coValue': '0.3',
         'dataTime': '2021-09-27 05:00',
         'khaiGrade': '1',
         'khaiValue': '48',
         'no2Flag': None,
         'no2Grade': '1',
         'no2Value': '0.007',
         'o3Flag': None,
         'o3Grade': '1',
         'o3Value': '0.029',
         'pm10Flag': None,
         'pm10Grade': '1',
         'pm10Value': '4',
         'pm25Flag': None,
         'pm25Grade': '1',
         'pm25Value': '2',
         'so2Flag': None,
         'so2Grade': '1',
         'so2Value': '0.002'},
        {'coFlag': None,
         'coGrade': '1',
         'coValue': '0.3',
         'dataTime': '2021-09-27 04:00',
         'khaiGrade': '1',
         'khaiValue': '50',
         'no2Flag': None,
         'no2Grade': '1',
         'no2Value': '0.007',
         'o3Flag': None,
         'o3Grade': '1',
         'o3Value': '0.030',
         'pm10Flag': None,
         'pm10Grade': '1',
         'pm10Value': '3',
         'pm25Flag': None,
         'pm25Grade': '1',
         'pm25Value': '1',
         'so2Flag': None,
         'so2Grade': '1',
         'so2Value': '0.003'},
        {'coFlag': None,
         'coGrade': '1',
         'coValue': '0.3',
         'dataTime': '2021-09-27 03:00',
         'khaiGrade': '2',
         'khaiValue': '51',
         'no2Flag': None,
         'no2Grade': '1',
         'no2Value': '0.005',
         'o3Flag': None,
         'o3Grade': '2',
         'o3Value': '0.031',
         'pm10Flag': None,
         'pm10Grade': '1',
         'pm10Value': '5',
         'pm25Flag': None,
         'pm25Grade': '1',
         'pm25Value': '2',
         'so2Flag': None,
         'so2Grade': '1',
         'so2Value': '0.002'},
        {'coFlag': None,
         'coGrade': '1',
         'coValue': '0.3',
         'dataTime': '2021-09-27 02:00',
         'khaiGrade': '2',
         'khaiValue': '51',
         'no2Flag': None,
         'no2Grade': '1',
         'no2Value': '0.006',
         'o3Flag': None,
         'o3Grade': '2',
         'o3Value': '0.031',
         'pm10Flag': None,
         'pm10Grade': '1',
         'pm10Value': '3',
         'pm25Flag': None,
         'pm25Grade': '1',
         'pm25Value': '1',
         'so2Flag': None,
         'so2Grade': '1',
         'so2Value': '0.003'}],
       'numOfRows': 5,
       'pageNo': 1,
       'totalCount': 23},
      'header': {'resultCode': '00', 'resultMsg': 'NORMAL_CODE'}}}




```python
o3_list = []
data1 = raw_dict["response"]["body"]["items"]
for data2 in data1:
    o3_list.append(data2["o3Value"])

o3_list
```




    ['0.028', '0.029', '0.030', '0.031', '0.031']




```python
numbers = ['one', 'two', 'three', 'four', 'five']
    
for n in numbers:
    print(n)
```

    one
    two
    three
    four
    five

