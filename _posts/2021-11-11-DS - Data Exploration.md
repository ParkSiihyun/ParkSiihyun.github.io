**3. Data Exploration**

*탐색적 데이터 분석은 우리가 존재한다고 믿는 것들은 물론이고 존재하지 않는 다고 믿는 것들을 발견하려는 태도, 유연성, 그리고 자발성이다*
*그림의 가장 큰 가치는 우리가 전혀 예상하지 못했던 것을 알아 차리게 될 때입니다*
* 주로 시각화하면서 우리가 발견하지 못했던 것을 발견할 수 있다.
* 탐색적 데이터 분석의 주된 수단 : 원본 데이터 관찰, 요약 통계값, 시각화
* 속성 간 관계를 분석하는 데 유리


---
**속성-속성 유형에 따른 시각화 방법**

* 수치–수치 – 상관 계수 – 산점도(scatter plot)
* 카테고리-수치 – 카테고리별 통계값(groupby()) – 막대그래프(bar plot), 박스플룻(상자그림)(box plot)
* 카테고리-카테고리 – 교차 테이블 – 히트맵(heat map), 모자이크 플룻(mosaic plot)



1. Correlation coefficient(상관계수)
* 상관계수는 두변수 값들이 서로 양의 관계가 강하면 1 서로 음의 관계가 강하면 -1 서로 관계가 없으면 0에 가까운 값을 가진다


```python
import pandas as pd
import seaborn as sns
import datetime as dt
import matplotlib as mtl

titanic_data = pd.read_csv("titanic.csv")
titanic_data["Sex"] = titanic_data["Sex"].map({"male" : 1, "female" : 0})
AAPL_data = pd.read_csv("AAPL.csv")
tips_data = pd.read_csv("tips.csv")

titanic_data.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
    
    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>1</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>0</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss. Laina</td>
      <td>0</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>0</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>1</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
  </tbody>
</table>
</div>




```python
titanic_data.corr().abs().sort_values("Survived", ascending=False) 
# df.corr() 함수를 이용하면 수치데이터 간의 상관계수를 알 수 있다. 
# abs(), sort_values()를 활용하면 직관적으로 어느 속성간의 관계를 직관적으로 파악할 수 있다. 
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
    
    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Fare</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Survived</th>
      <td>0.005007</td>
      <td>1.000000</td>
      <td>0.338481</td>
      <td>0.543351</td>
      <td>0.077221</td>
      <td>0.035322</td>
      <td>0.081629</td>
      <td>0.257307</td>
    </tr>
    <tr>
      <th>Sex</th>
      <td>0.042939</td>
      <td>0.543351</td>
      <td>0.131900</td>
      <td>1.000000</td>
      <td>0.093254</td>
      <td>0.114631</td>
      <td>0.245489</td>
      <td>0.182333</td>
    </tr>
    <tr>
      <th>Pclass</th>
      <td>0.035144</td>
      <td>0.338481</td>
      <td>1.000000</td>
      <td>0.131900</td>
      <td>0.369226</td>
      <td>0.083081</td>
      <td>0.018443</td>
      <td>0.549500</td>
    </tr>
    <tr>
      <th>Fare</th>
      <td>0.012658</td>
      <td>0.257307</td>
      <td>0.549500</td>
      <td>0.182333</td>
      <td>0.096067</td>
      <td>0.159651</td>
      <td>0.216225</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>Parch</th>
      <td>0.001652</td>
      <td>0.081629</td>
      <td>0.018443</td>
      <td>0.245489</td>
      <td>0.189119</td>
      <td>0.414838</td>
      <td>1.000000</td>
      <td>0.216225</td>
    </tr>
    <tr>
      <th>Age</th>
      <td>0.036847</td>
      <td>0.077221</td>
      <td>0.369226</td>
      <td>0.093254</td>
      <td>1.000000</td>
      <td>0.308247</td>
      <td>0.189119</td>
      <td>0.096067</td>
    </tr>
    <tr>
      <th>SibSp</th>
      <td>0.057527</td>
      <td>0.035322</td>
      <td>0.083081</td>
      <td>0.114631</td>
      <td>0.308247</td>
      <td>1.000000</td>
      <td>0.414838</td>
      <td>0.159651</td>
    </tr>
    <tr>
      <th>PassengerId</th>
      <td>1.000000</td>
      <td>0.005007</td>
      <td>0.035144</td>
      <td>0.042939</td>
      <td>0.036847</td>
      <td>0.057527</td>
      <td>0.001652</td>
      <td>0.012658</td>
    </tr>
  </tbody>
</table>
</div>



2. Line Plot Chart(꺾은 선 그래프)

* x 축 값만 지정하게 된다면 수치로 되어있는 나머지 열 값을 모두 그래프로 나타내준다
* y 축 값도 지정하게 된다면 하나의 열과 x축과의 관계만이 보인다.
* Y 축 값은 리스트 형태로 여러개를 지정할 수 있다. 
* 시계열 데이터 표현에 적합. 



```python
temp_dict = {"Month":[1, 2, 3, 4], 
             "Temperature":[4, 8, 15, 18], 
             "Humidity":[32, 35, 41, 52],
             "Dust(average)":[15.4, 21.2, 68.8, 72.1]}

df1 = pd.DataFrame(temp_dict)
df_line = df1.plot.line(x="Month", y=["Humidity","Dust(average)"],style=["o-r", "*--g"])
# 우선 선 플롯 차트를 불러오기 위해서는 df.plot.line(x="column_name", y="column_name")
# title= 패러미터로 그래프에 이름을 설정할 수 있다
# style=["점의 형태 선의형태 선의색깔"] ex) style=["o--r"]

df_line
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8c35fed0>




​    
![png](output_5_1.png)
​    



```python
AAPL_data["date"] = pd.to_datetime(AAPL_data["date"])
AAPL_data = AAPL_data.rename(columns={"close" : "price"}) # DataFrame의 column name 바꾸는 함수 rename(columns={oldname : newname})

AAPL_data_line = AAPL_data.plot.line(x="date", y="price",title="Apple Stock Price", style=["r"]) 
```


​    
![png](output_6_0.png)
​    


3. Bar Chart

* Category(범주형 데이터 표현에 적합)


```python
data = {"Category":["A", "B", "C"],
        "Value1":[10, 21, 19],
        "Value2":[20, 11, 8]}

df2 = pd.DataFrame(data)
df_bar = df4.plot.bar(x="Category")
# 우선 바 플롯 차트를 불러오기 위해서는 df.plot.bar(x="column_name", y="column_name")
# title= 패러미터로 그래프에 이름을 설정할 수 있다
# color=["color1", "color2"] 

df_bar
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8c28f790>




​    
![png](output_8_1.png)
​    



```python
AAPL_data["date"] = pd.to_datetime(AAPL_data["date"])
AAPL_data_bar = AAPL_data[0:10].plot.bar(x="date", y="volume", color=["blue"], ylim=[20000000,60000000], title="sale_volume")

AAPL_data_bar
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8c1f8410>




​    
![png](output_9_1.png)
​    


4. 그래프 병합(line-line, line bar)


```python
df_bar = df2.plot.bar(x="Category", y="Value1")
df_line_bar = df2.plot.line(x="Category", y="Value2", ax=df_bar) # ax=추가할 그래프 변수명, 하나의 데이터에서만 가능(?)
```


​    
![png](output_11_0.png)
​    


5. 산점도(scatter plot)
* 두 변수 간의 상관관계 파악
* 데이터 분석에서 가장 자주 사용됨
* 데이터의 군집을 파악할 때도 쓰임(좋은 콜레스테롤, 나쁜 콜레스테롤을 두 변수로 두는 경우)



```python
Iris_data = pd.read_csv("Iris.csv").drop(["Id"], axis=1)

Iris_data.plot.scatter(x="SepalLengthCm", y="SepalWidthCm")
```

    *c* argument looks like a single numeric RGB or RGBA sequence, which should be avoided as value-mapping will have precedence in case its length matches with *x* & *y*.  Please use the *color* keyword-argument or provide a 2-D array with a single row if you intend to specify the same RGB or RGBA value for all points.





    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8c0e7c10>




​    
![png](output_13_2.png)
​    


6. Histogram(히스토그램)

* 변수의 구간별 빈도수를 나타낸 그래프
* 막대그래프와는 달리 값 사이사이에 공백이 없음



```python
Iris_data["SepalLengthCm"].plot.hist(bins=5) # data.plot.hist(bins=구간의 개수)
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8c0f9b90>




​    
![png](output_15_1.png)
​    



```python
Iris_data["SepalLengthCm"].plot.hist(bins=[4,5,6,7,8]) # dataframe.plot.hist(bins=[구간의 리스트])
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8bff0f10>




​    
![png](output_16_1.png)
​    


7. Box Plot(상자 그림)
* 데이터 값을 그대로 그래프로 나타내는 것이 아니라 통계 정보를 시각화하는 것이 특징* 5가지 통계정보 
* min(q2+1.5xbox height) q1 q2 q3 max(q2-1.5*box height) 값을 보여줌
* 수치 – 카테고리 간의 비교에 적합, 분포확인에 적합
* 이상값 확인에 용이
* 요즘에는 violin plot(상자그림과 유사)



```python
Iris_data.boxplot() # df.plot.box()아님 주의하자 df.boxplot()WidthCm"]
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8bf87990>




​    
![png](output_18_1.png)
​    


8. 그래프는 그려지는데 한국어로 된 column_name이 안나온다? 

* 한글을 나타낼 수 잇는 폰트가 없어서 발생하는 문제 
* impot matplotlib.pyplot as plt
* plt.re(“font”, family=”AppleGothic”) 라는 구문을 사용하자 

9. Seaborn의 시각화 기능

---
9-1. Linear Regression Model Plot(선형 회귀 모델) 그리기



```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

sns.lmplot(x="PetalWidthCm", y="PetalLengthCm", data=Iris_data) 
# sns.lmplot(x=, y=, data=) 
# 선형모델을 생성하여 예측선(추세선)을 그려준다
```




    <seaborn.axisgrid.FacetGrid at 0x7f6a8beb2fd0>




​    
![png](output_21_1.png)
​    



```python
sns.lmplot(x="PetalWidthCm", y="PetalLengthCm", data=Iris_data, hue="Species") # hue 패러미터를 사용해 Category 별로 다른 색을 지정할 수 있다. 
```




    <seaborn.axisgrid.FacetGrid at 0x7f6a8beb2c50>




​    
![png](output_22_1.png)
​    


9-2. scatterplot(산점도 그리기)


```python
sns.scatterplot(x="PetalWidthCm", y="PetalLengthCm", data=Iris_data, hue="Species") 
# lmplot을 사용해도 산점도를 나타낼 수 있지만 꽃잎과 같은 데이터는 추세선이 필요없으므로 sns.scatterplot()기능을 사용해도 된다. 

```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8bdcf1d0>




​    
![png](output_24_1.png)
​    


9-3. boxplot(상자그림 그리기)


```python
sns.boxplot(x="sex", y="total_bill",data=tips_data) #sns.boxplot(x=, y=, data=)
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8bd3acd0>




​    
![png](output_26_1.png)
​    



```python
sns.boxplot(x="smoker", y="total_bill",data=tips_data) 
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8bcb2c10>




​    
![png](output_27_1.png)
​    


9-4. Pair Grid

* 복수(두개 말고 여러개)의 속성간의 관계를 격자 구조에 모두 표현



```python
grid = sns.PairGrid(Iris_data, hue="Species")
grid.map(plt.scatter)
```




    <seaborn.axisgrid.PairGrid at 0x7f6a8bc6c0d0>




​    
![png](output_29_1.png)
​    


9-5. PairGrid 대각선 채우기


```python
# 대각선 부분은 같은 속성끼리의 관계므로 무의미하다. 
# 대각선 부분을 다른 그래프로 채워보자. 

grid = sns.PairGrid(Iris_data, hue="Species")
grid.map_diag(plt.hist) # map_diag(sth) 대각선인 부분은 sth로 채워라
grid.map_offdiag(plt.scatter) # map_offdiag(sth) 대각선이 아닌 부분은 산점도로 채워라
grid.add_legend(); #legend 범례도 설정할 수 있다.
```


​    
![png](output_31_0.png)
​    


9-6. Heat Map(히트맵)

* 데이터의 값을 열(heat)의 분포 형태로 시각화 시킨 이미지
* 두 개의 카테고리 값을 시각화 할 때 유용
* 카테고리 간의 관계 혹은 군집(cluster)를 확인



```python
import matplotlib.pyplot as plt
plt.figure(figsize=(15, 10))
sns.set(font_scale=0.8)

crime_data = pd.read_csv("Berlin_crimes.csv")
crime_data = crime_data.groupby("Year", as_index=False).sum().drop(["Year","Code"], axis=1)
crime_data.index = [2012,2013,2014,2015,2016,2017,2018,2019] # index에 지정할 Category를 list로 저장해준다. 

sns.heatmap(crime_data, annot=True, fmt="d", cmap="coolwarm") # sns.heatmap(data)의 형태
# annot=True : 주석을 표시해라
# fmt='d' : 주석은 정수의 형태로 fmt='.2f' : 주석은 소수점 둘째자리까지
# cmap="coolwarm" : 색은 coolwarm 으로

```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f6a8aa3c1d0>




​    
![png](output_33_1.png)
​    

