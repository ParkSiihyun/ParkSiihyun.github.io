**2. Data Preparation**

* 데이터를 분석에 적합한 형태로 가공한다.
* 분석 소프트웨어가 읽을 수 있는 정형화된 데이터로 준비한다.

* 1. 테이블 형태 : CSV
* ex) 웹 스크래핑이나 Open API로 얻은 HTML이나 XML을 CSV로 변환
* 2. JSON, SQL, ... etc


3. Tabular Data 
* 데이터는 테이블이라고 봐도 무방하다
* 데이터의 절대 다수가 테이블 형태로 존재하거나 테이블로 변환될 수 있다.
* 인간과 컴퓨터가 이해하고 처리하기에 편리한 구조
* 열(column)=속성(feature)과 행(row)=항목(item)이 있다.

4. CSV

* 쉼표로 데이터의 열을 구분하고 줄 바꿈으로 행을 구분하여 표 형식의 데이터를 저장하는 텍스트 파일 형식

5. Pandas Module

* 데이터의 표현 및 분석을 위한 Python Module
* 표 형식의 데이터 처리와 관련된 다양한 기능 제공
* 표를 데이터프레임(DataFrame)이라는 구조로 표현
* DataFrame : column, row, index로 구성된 형식


```python
import pandas as pd # pandas 모듈을 불러오는 방법, import a as b : a라는 모듈을 이하 b라고 이른다.

data_dict = { "food" : ["apple","banana", "pear"], "animal" : ["cat","dog","zebra"]} # 딕셔너리로 표 데이터를 만들면 column named을 설정할 수 있다.
A = pd.DataFrame(data_dict)

print(A)
```

         food animal
    0   apple    cat
    1  banana    dog
    2    pear  zebra


6.	Series
* Pandas에는 Series라는 자료 구조가 있다. 
*	1차원 리스트와 비슷한 구조
*	표 데이터에서 한 개의 열에 해당하는 값을 표현
*	Data frame에서 하나의 열을 가져오면 Series의 형태로 표현됨. 



```python
print(A["animal"]) # 결과값은 Series의 형태이다
```

    0      cat
    1      dog
    2    zebra
    Name: animal, dtype: object


7. Creating DataFrame

7-1. column name 설정하기


```python
data = [[23,45,25],[23,67,34],[67,46,87]]
df = pd.DataFrame(data) # 리스트로 만든 표데이터는 column name을 설정할 수 있다.
df.columns = ["a", "b", "c"]

print(df)
```

        a   b   c
    0  23  45  25
    1  23  67  34
    2  67  46  87


7-2. CSV 및 xlsx 파일을을 DataFrame으로로 변환하기


```python
df1 = pd.read_csv("heart.csv") # pd.read.csv() 함수를 사용하면 csv 파일을 DataFrame으로 바꿀꿀 수 있다.
# 유니코드 오류시 ("filename", encoding="euc-kr")

print(df1)
```

         age  sex  cp  trestbps  chol  fbs  ...  exang  oldpeak  slope  ca  thal  target
    0     63    1   3       145   233    1  ...      0      2.3      0   0     1       1
    1     37    1   2       130   250    0  ...      0      3.5      0   0     2       1
    2     41    0   1       130   204    0  ...      0      1.4      2   0     2       1
    3     56    1   1       120   236    0  ...      0      0.8      2   0     2       1
    4     57    0   0       120   354    0  ...      1      0.6      2   0     2       1
    ..   ...  ...  ..       ...   ...  ...  ...    ...      ...    ...  ..   ...     ...
    298   57    0   0       140   241    0  ...      1      0.2      1   0     3       0
    299   45    1   3       110   264    0  ...      0      1.2      1   0     3       0
    300   68    1   0       144   193    1  ...      0      3.4      1   2     3       0
    301   57    1   0       130   131    0  ...      1      1.2      1   1     3       0
    302   57    0   1       130   236    0  ...      0      0.0      1   1     2       0
    
    [303 rows x 14 columns]



```python
df2 = pd.read_excel("StudentsPerformance2.xlsx") # pd.read.excel() 함수를 사용하면 excel 파일을 DataFrame으로 바꿀꿀 수 있다.
# 유니코드 오류시 ("filename", encoding="euc-kr")

print(df2)
```

         gender race/ethnicity  ... reading score writing score
    0    female        group B  ...            72            74
    1    female        group C  ...            90            88
    2    female        group B  ...            95            93
    3      male        group A  ...            57            44
    4      male        group C  ...            78            75
    ..      ...            ...  ...           ...           ...
    995  female        group E  ...            99            95
    996    male        group C  ...            55            55
    997  female        group C  ...            71            65
    998  female        group D  ...            78            77
    999  female        group D  ...            86            86
    
    [1000 rows x 8 columns]


7-3. index name 설정하기


```python
mean = {"class1" : [78.567,67.545,89.565], "class2" : [56.786,78.546,98.567], "class3" : [45.575,69.564,59.342]}

indexed_mean = pd.DataFrame(mean)

indexed_mean.index = ["A", "B", "C"] # df.columns 는 열이름, df.index 는 행이름 설정

indexed_mean
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
      <th>class1</th>
      <th>class2</th>
      <th>class3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>A</th>
      <td>78.567</td>
      <td>56.786</td>
      <td>45.575</td>
    </tr>
    <tr>
      <th>B</th>
      <td>67.545</td>
      <td>78.546</td>
      <td>69.564</td>
    </tr>
    <tr>
      <th>C</th>
      <td>89.565</td>
      <td>98.567</td>
      <td>59.342</td>
    </tr>
  </tbody>
</table>
</div>



8. selecting Data(특정 열만 추출하기)


```python
print(df2["gender"]) # 전체 DataFrame에서 ["column_name"]을 붙여주면 특정 열만 추출된다.
```

    0      female
    1      female
    2      female
    3        male
    4        male
            ...  
    995    female
    996      male
    997    female
    998    female
    999    female
    Name: gender, Length: 1000, dtype: object



```python
print(df1[["age","sex"]]) # 전체 DataFrame에서 여러개의 열을 추출할 때는 list속에 column_name을 나열한다.
```

         age  sex
    0     63    1
    1     37    1
    2     41    0
    3     56    1
    4     57    0
    ..   ...  ...
    298   57    0
    299   45    1
    300   68    1
    301   57    1
    302   57    0
    
    [303 rows x 2 columns]


9. Dropping Columns(지정한 열을 제외하기)


```python
print(df1.drop(["slope"], axis=1)) # drop(["column name"], axis=1)의 형식으로 제외하고 싶은 열을 제외한다.
```

         age  sex  cp  trestbps  chol  ...  exang  oldpeak  ca  thal  target
    0     63    1   3       145   233  ...      0      2.3   0     1       1
    1     37    1   2       130   250  ...      0      3.5   0     2       1
    2     41    0   1       130   204  ...      0      1.4   0     2       1
    3     56    1   1       120   236  ...      0      0.8   0     2       1
    4     57    0   0       120   354  ...      1      0.6   0     2       1
    ..   ...  ...  ..       ...   ...  ...    ...      ...  ..   ...     ...
    298   57    0   0       140   241  ...      1      0.2   0     3       0
    299   45    1   3       110   264  ...      0      1.2   0     3       0
    300   68    1   0       144   193  ...      0      3.4   2     3       0
    301   57    1   0       130   131  ...      1      1.2   1     3       0
    302   57    0   1       130   236  ...      0      0.0   1     2       0
    
    [303 rows x 13 columns]



```python
print(df1.drop(["age","chol"], axis=1)) 
# drop(["column name1, column name2"], axis=1)
# 열을 호출하는 df["column name"]과 헷갈리지 말자
```

         sex  cp  trestbps  fbs  restecg  ...  oldpeak  slope  ca  thal  target
    0      1   3       145    1        0  ...      2.3      0   0     1       1
    1      1   2       130    0        1  ...      3.5      0   0     2       1
    2      0   1       130    0        0  ...      1.4      2   0     2       1
    3      1   1       120    0        1  ...      0.8      2   0     2       1
    4      0   0       120    0        1  ...      0.6      2   0     2       1
    ..   ...  ..       ...  ...      ...  ...      ...    ...  ..   ...     ...
    298    0   0       140    0        1  ...      0.2      1   0     3       0
    299    1   3       110    0        1  ...      1.2      1   0     3       0
    300    1   0       144    1        1  ...      3.4      1   2     3       0
    301    1   0       130    0        1  ...      1.2      1   1     3       0
    302    0   1       130    0        0  ...      0.0      1   1     2       0
    
    [303 rows x 12 columns]


10. Basic Data Analysis(데이터의 기본적인 정보 파악하기)


```python
df1.shape # shape는 DataFrame의 행과 열의 갯수를 알려준다.(행,열), 괄호는 필요없음
```




    (303, 14)




```python
df1.describe() # describe() 함수는 데이터의 갯수, 평균, 표준편차, 최솟값, 사분위수, 최댓값 과 같은 데이터의 기본적인 정보들을 알려준다.
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
      <th>age</th>
      <th>sex</th>
      <th>cp</th>
      <th>trestbps</th>
      <th>chol</th>
      <th>fbs</th>
      <th>restecg</th>
      <th>thalach</th>
      <th>exang</th>
      <th>oldpeak</th>
      <th>slope</th>
      <th>ca</th>
      <th>thal</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
      <td>303.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>54.366337</td>
      <td>0.683168</td>
      <td>0.966997</td>
      <td>131.623762</td>
      <td>246.264026</td>
      <td>0.148515</td>
      <td>0.528053</td>
      <td>149.646865</td>
      <td>0.326733</td>
      <td>1.039604</td>
      <td>1.399340</td>
      <td>0.729373</td>
      <td>2.313531</td>
      <td>0.544554</td>
    </tr>
    <tr>
      <th>std</th>
      <td>9.082101</td>
      <td>0.466011</td>
      <td>1.032052</td>
      <td>17.538143</td>
      <td>51.830751</td>
      <td>0.356198</td>
      <td>0.525860</td>
      <td>22.905161</td>
      <td>0.469794</td>
      <td>1.161075</td>
      <td>0.616226</td>
      <td>1.022606</td>
      <td>0.612277</td>
      <td>0.498835</td>
    </tr>
    <tr>
      <th>min</th>
      <td>29.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>94.000000</td>
      <td>126.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>71.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>47.500000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>120.000000</td>
      <td>211.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>133.500000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>55.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>130.000000</td>
      <td>240.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>153.000000</td>
      <td>0.000000</td>
      <td>0.800000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>61.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>140.000000</td>
      <td>274.500000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>166.000000</td>
      <td>1.000000</td>
      <td>1.600000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>77.000000</td>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>200.000000</td>
      <td>564.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>202.000000</td>
      <td>1.000000</td>
      <td>6.200000</td>
      <td>2.000000</td>
      <td>4.000000</td>
      <td>3.000000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.mean()
df1.std()
df.count()
df.mode() # 최빈값
df.min()
df.sum() # 합계
df1.median() # 같이 함수를 직접 사용해 필요한 값들을 불러올 수 있다.
```




    age          55.0
    sex           1.0
    cp            1.0
    trestbps    130.0
    chol        240.0
    fbs           0.0
    restecg       1.0
    thalach     153.0
    exang         0.0
    oldpeak       0.8
    slope         1.0
    ca            0.0
    thal          2.0
    target        1.0
    dtype: float64




```python
print(df1.head(), df1.tail()) # .head(), .tail() 함수를 활용해 데이터의 첫부분과 꼬리부분을 추출할 수 있다.
```

       age  sex  cp  trestbps  chol  fbs  ...  exang  oldpeak  slope  ca  thal  target
    0   63    1   3       145   233    1  ...      0      2.3      0   0     1       1
    1   37    1   2       130   250    0  ...      0      3.5      0   0     2       1
    2   41    0   1       130   204    0  ...      0      1.4      2   0     2       1
    3   56    1   1       120   236    0  ...      0      0.8      2   0     2       1
    4   57    0   0       120   354    0  ...      1      0.6      2   0     2       1
    
    [5 rows x 14 columns]      age  sex  cp  trestbps  chol  fbs  ...  exang  oldpeak  slope  ca  thal  target
    298   57    0   0       140   241    0  ...      1      0.2      1   0     3       0
    299   45    1   3       110   264    0  ...      0      1.2      1   0     3       0
    300   68    1   0       144   193    1  ...      0      3.4      1   2     3       0
    301   57    1   0       130   131    0  ...      1      1.2      1   1     3       0
    302   57    0   1       130   236    0  ...      0      0.0      1   1     2       0
    
    [5 rows x 14 columns]



```python
df1["age"].mode()[0] # 최빈값 series에서 첫번째 최빈값만을 얻기 위해서 첫번째 행에 해당하는 index[0]을 붙여준다.
```




    58




```python
df1["age"].abs() # 데이터들의 절댓값을 얻을 수 있는 함수
```




    0      63
    1      37
    2      41
    3      56
    4      57
           ..
    298    57
    299    45
    300    68
    301    57
    302    57
    Name: age, Length: 303, dtype: int64



11. 데이터의 column 값으로 row 선택하기


```python
df_new = df1[df1["age"] >= 60] # df[df["column name"] == or >= or <...etc]의 형식으로 열의 조건을 추가할 수 있다.

print(df_new.head())
```

        age  sex  cp  trestbps  chol  fbs  ...  exang  oldpeak  slope  ca  thal  target
    0    63    1   3       145   233    1  ...      0      2.3      0   0     1       1
    13   64    1   3       110   211    0  ...      1      1.8      1   0     2       1
    17   66    0   3       150   226    0  ...      0      2.6      0   0     2       1
    19   69    0   3       140   239    0  ...      0      1.8      2   2     2       1
    23   61    1   2       150   243    1  ...      1      1.0      1   0     2       1
    
    [5 rows x 14 columns]



```python
df_new = df1[(df1["age"] >= 60) & (df1["sex"] == 1)] # 위와 같은 방식이지만 여러개의 열을 연결할 때는 (cond1)&(cond2) 형식을 사용한다. 형식주의!

print(df_new.head())
```

        age  sex  cp  trestbps  chol  fbs  ...  exang  oldpeak  slope  ca  thal  target
    0    63    1   3       145   233    1  ...      0      2.3      0   0     1       1
    13   64    1   3       110   211    0  ...      1      1.8      1   0     2       1
    23   61    1   2       150   243    1  ...      1      1.0      1   0     2       1
    31   65    1   0       120   177    0  ...      0      0.4      2   0     3       1
    51   66    1   0       120   302    0  ...      0      0.4      1   0     2       1
    
    [5 rows x 14 columns]


12. Grouping Table(그룹별 집계하기 함수 : groupby())


```python
df_new = df1.groupby(["sex"], as_index=False).mean() 
# df.groupdy(df["sex"], as_index=False)를 하면 sex열에서 같은 것끼리 묶인다.
# .mean()을 추가하면 묶인 값들의 평균이 구해진다.

print(df_new)
```

       sex        age        cp    trestbps  ...     slope        ca      thal    target
    0    0  55.677083  1.041667  133.083333  ...  1.427083  0.552083  2.125000  0.750000
    1    1  53.758454  0.932367  130.946860  ...  1.386473  0.811594  2.400966  0.449275
    
    [2 rows x 14 columns]



```python
df_new = df1.groupby(["sex", "age"], as_index=False).sum() # groupby 함수에 여러 개의 column을 나열하면 1차적 기준, 2차적 기준이 된다. 

df_new 
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
      <th>sex</th>
      <th>age</th>
      <th>cp</th>
      <th>trestbps</th>
      <th>chol</th>
      <th>fbs</th>
      <th>restecg</th>
      <th>thalach</th>
      <th>exang</th>
      <th>oldpeak</th>
      <th>slope</th>
      <th>ca</th>
      <th>thal</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>34</td>
      <td>1</td>
      <td>118</td>
      <td>210</td>
      <td>0</td>
      <td>1</td>
      <td>192</td>
      <td>0</td>
      <td>0.7</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0</td>
      <td>35</td>
      <td>0</td>
      <td>138</td>
      <td>183</td>
      <td>0</td>
      <td>1</td>
      <td>182</td>
      <td>0</td>
      <td>1.4</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>37</td>
      <td>2</td>
      <td>120</td>
      <td>215</td>
      <td>0</td>
      <td>1</td>
      <td>170</td>
      <td>0</td>
      <td>0.0</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>39</td>
      <td>4</td>
      <td>232</td>
      <td>419</td>
      <td>0</td>
      <td>2</td>
      <td>331</td>
      <td>0</td>
      <td>0.0</td>
      <td>3</td>
      <td>0</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>41</td>
      <td>5</td>
      <td>473</td>
      <td>976</td>
      <td>0</td>
      <td>2</td>
      <td>675</td>
      <td>1</td>
      <td>1.4</td>
      <td>8</td>
      <td>1</td>
      <td>8</td>
      <td>4</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>68</th>
      <td>1</td>
      <td>67</td>
      <td>2</td>
      <td>777</td>
      <td>1517</td>
      <td>1</td>
      <td>2</td>
      <td>746</td>
      <td>3</td>
      <td>7.0</td>
      <td>6</td>
      <td>9</td>
      <td>15</td>
      <td>0</td>
    </tr>
    <tr>
      <th>69</th>
      <td>1</td>
      <td>68</td>
      <td>4</td>
      <td>442</td>
      <td>744</td>
      <td>2</td>
      <td>2</td>
      <td>442</td>
      <td>1</td>
      <td>6.0</td>
      <td>4</td>
      <td>3</td>
      <td>9</td>
      <td>1</td>
    </tr>
    <tr>
      <th>70</th>
      <td>1</td>
      <td>69</td>
      <td>5</td>
      <td>300</td>
      <td>488</td>
      <td>1</td>
      <td>0</td>
      <td>277</td>
      <td>0</td>
      <td>2.1</td>
      <td>2</td>
      <td>4</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>71</th>
      <td>1</td>
      <td>70</td>
      <td>3</td>
      <td>591</td>
      <td>1010</td>
      <td>0</td>
      <td>2</td>
      <td>489</td>
      <td>2</td>
      <td>7.9</td>
      <td>4</td>
      <td>4</td>
      <td>10</td>
      <td>1</td>
    </tr>
    <tr>
      <th>72</th>
      <td>1</td>
      <td>77</td>
      <td>0</td>
      <td>125</td>
      <td>304</td>
      <td>0</td>
      <td>0</td>
      <td>162</td>
      <td>1</td>
      <td>0.0</td>
      <td>2</td>
      <td>3</td>
      <td>2</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>73 rows × 14 columns</p>
</div>



13. 항목 추출하기 : 중복되는 값들을 하나로 만들어주기


```python
age_list = df1["age"].unique() # 추출하고 싶은 열을 선택하고 .unique() 함수를 이용하면 항목들을 리스트로 반환받을 수 있다.
sex_list = df1["sex"].unique()
print(age_list, sex_list)
```

    [63 37 41 56 57 44 52 54 48 49 64 58 50 66 43 69 59 42 61 40 71 51 65 53
     46 45 39 47 62 34 35 29 55 60 67 68 74 76 70 38 77] [1 0]


14. Rounding Numbers


```python
mean = {"class1" : [78.567,67.545,89.565], "class2" : [56.786,78.546,98.567], "class3" : [45.575,69.564,59.342]}
df_mean = pd.DataFrame(mean)

df_mean_rounded_1 = df_mean.round(1) # 파이썬 기초의 round() 함수와 사용법은 동일하다.
df_mean_rounded_2 = df_mean.round(-1)
df_mean_rounded_3 = df_mean["class1"].round(1) # 특정 열의 수치만 반올림 가능하다. 

print(df_mean)
print(df_mean_rounded_1)
print(df_mean_rounded_2)
print(df_mean_rounded_3)
```

       class1  class2  class3
    0  78.567  56.786  45.575
    1  67.545  78.546  69.564
    2  89.565  98.567  59.342
       class1  class2  class3
    0    78.6    56.8    45.6
    1    67.5    78.5    69.6
    2    89.6    98.6    59.3
       class1  class2  class3
    0    80.0    60.0    50.0
    1    70.0    80.0    70.0
    2    90.0   100.0    60.0
    0    78.6
    1    67.5
    2    89.6
    Name: class1, dtype: float64


15. Changing Datatype


```python
print(df_mean.astype(int)) # .astype() 함수를 사용하면 데이터프레임 속의 데이터형의 변환이 가능하다
print(df_mean["class1"].astype(int)) # 특정 열의 데이터형의 변환이 가능하다

```

       class1  class2  class3
    0      78      56      45
    1      67      78      69
    2      89      98      59
    0    78
    1    67
    2    89
    Name: class1, dtype: int64


16. 정렬


```python
print(df_mean.sort_values("class1", ascending=True)) # .sort_values("column", ascending=True)를 사용하면 "column"열을 1차적 기준으로 오름차순 정렬된다.
```

       class1  class2  class3
    1  67.545  78.546  69.564
    0  78.567  56.786  45.575
    2  89.565  98.567  59.342



```python
print(df_mean.sort_values("class1", ascending=False)) # .sort_values("column", ascending=False)를 사용하면 "column"열을 1차적 기준으로 내림차순 정렬된다.
```

       class1  class2  class3
    2  89.565  98.567  59.342
    0  78.567  56.786  45.575
    1  67.545  78.546  69.564



```python
print(df_mean.sort_values(["class1", "class3"], ascending=False)) # "column"을 리스트로 묶어 여러개의 값으로 지정하면 그 순서대로 1차적 기준, 2차적 기준...이 된다.
```

       class1  class2  class3
    2  89.565  98.567  59.342
    0  78.567  56.786  45.575
    1  67.545  78.546  69.564


17. Slicing DataFrame


```python
df1[5:12] # List의 슬라이싱 기법과 동일하다
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
      <th>age</th>
      <th>sex</th>
      <th>cp</th>
      <th>trestbps</th>
      <th>chol</th>
      <th>fbs</th>
      <th>restecg</th>
      <th>thalach</th>
      <th>exang</th>
      <th>oldpeak</th>
      <th>slope</th>
      <th>ca</th>
      <th>thal</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5</th>
      <td>57</td>
      <td>1</td>
      <td>0</td>
      <td>140</td>
      <td>192</td>
      <td>0</td>
      <td>1</td>
      <td>148</td>
      <td>0</td>
      <td>0.4</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>56</td>
      <td>0</td>
      <td>1</td>
      <td>140</td>
      <td>294</td>
      <td>0</td>
      <td>0</td>
      <td>153</td>
      <td>0</td>
      <td>1.3</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>44</td>
      <td>1</td>
      <td>1</td>
      <td>120</td>
      <td>263</td>
      <td>0</td>
      <td>1</td>
      <td>173</td>
      <td>0</td>
      <td>0.0</td>
      <td>2</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>52</td>
      <td>1</td>
      <td>2</td>
      <td>172</td>
      <td>199</td>
      <td>1</td>
      <td>1</td>
      <td>162</td>
      <td>0</td>
      <td>0.5</td>
      <td>2</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>57</td>
      <td>1</td>
      <td>2</td>
      <td>150</td>
      <td>168</td>
      <td>0</td>
      <td>1</td>
      <td>174</td>
      <td>0</td>
      <td>1.6</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>54</td>
      <td>1</td>
      <td>0</td>
      <td>140</td>
      <td>239</td>
      <td>0</td>
      <td>1</td>
      <td>160</td>
      <td>0</td>
      <td>1.2</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>48</td>
      <td>0</td>
      <td>2</td>
      <td>130</td>
      <td>275</td>
      <td>0</td>
      <td>1</td>
      <td>139</td>
      <td>0</td>
      <td>0.2</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>



18. Adding New Data(새로운 열 추가하기 & 기존의 열 갱신하기)


```python
df_mean["class4"] = 0 # 딕셔너리 값에서 key값을 추가, 갱신하는 방법과 동일하다

print(df_mean)
```

       class1  class2  class3  class4
    0  78.567  56.786  45.575       0
    1  67.545  78.546  69.564       0
    2  89.565  98.567  59.342       0



```python
df_mean["class4"] = [78.435,89.345,45.546]

print(df_mean)
```

       class1  class2  class3  class4
    0  78.567  56.786  45.575  78.435
    1  67.545  78.546  69.564  89.345
    2  89.565  98.567  59.342  45.546



```python
df_mean["class5"] = df_mean["class4"] # 새로운 열을 추가할 때 리스트 뿐만 아니라 series의 형태로도 추가할 수 있다.

print(df_mean) 
```

       class1  class2  class3  class4  class5
    0  78.567  56.786  45.575  78.435  78.435
    1  67.545  78.546  69.564  89.345  89.345
    2  89.565  98.567  59.342  45.546  45.546


19. DataFrame의 열과 행을 선택할 수 있는 표기법 df.loc[ ]


```python
# df.loc[row_indexer, column_indexer]

df1.loc[3:12, ["age","sex"]] # index기준 3이상 12이하 행의 "age"와 "sex"열을 나타내라
df1.loc[200:231, "chol"] # index기준 200이상 231이하 행의 "chol"열을 나타내라
df1.loc[df1["age"] >= 70, "sex"] # "age"열이 70이상인 행의 "sex"열을 나타내라
df1.loc[:, "sex"] # 전체 행의 "sex"열을 나타내라
df1["survived"] = "pass"
cond = (df1["age"] >= 60) & (df1["sex"] == 1) # () | () or () & ()의 형식으로 행의 조건을 여러개 나열할 수 있다. | = or, & = and 
df1.loc[cond, "survived"] = "fail"

df1
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
      <th>age</th>
      <th>sex</th>
      <th>cp</th>
      <th>trestbps</th>
      <th>chol</th>
      <th>fbs</th>
      <th>restecg</th>
      <th>thalach</th>
      <th>exang</th>
      <th>oldpeak</th>
      <th>slope</th>
      <th>ca</th>
      <th>thal</th>
      <th>target</th>
      <th>survived</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>63</td>
      <td>1</td>
      <td>3</td>
      <td>145</td>
      <td>233</td>
      <td>1</td>
      <td>0</td>
      <td>150</td>
      <td>0</td>
      <td>2.3</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>1</th>
      <td>37</td>
      <td>1</td>
      <td>2</td>
      <td>130</td>
      <td>250</td>
      <td>0</td>
      <td>1</td>
      <td>187</td>
      <td>0</td>
      <td>3.5</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>2</th>
      <td>41</td>
      <td>0</td>
      <td>1</td>
      <td>130</td>
      <td>204</td>
      <td>0</td>
      <td>0</td>
      <td>172</td>
      <td>0</td>
      <td>1.4</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>3</th>
      <td>56</td>
      <td>1</td>
      <td>1</td>
      <td>120</td>
      <td>236</td>
      <td>0</td>
      <td>1</td>
      <td>178</td>
      <td>0</td>
      <td>0.8</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>4</th>
      <td>57</td>
      <td>0</td>
      <td>0</td>
      <td>120</td>
      <td>354</td>
      <td>0</td>
      <td>1</td>
      <td>163</td>
      <td>1</td>
      <td>0.6</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>298</th>
      <td>57</td>
      <td>0</td>
      <td>0</td>
      <td>140</td>
      <td>241</td>
      <td>0</td>
      <td>1</td>
      <td>123</td>
      <td>1</td>
      <td>0.2</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>299</th>
      <td>45</td>
      <td>1</td>
      <td>3</td>
      <td>110</td>
      <td>264</td>
      <td>0</td>
      <td>1</td>
      <td>132</td>
      <td>0</td>
      <td>1.2</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>300</th>
      <td>68</td>
      <td>1</td>
      <td>0</td>
      <td>144</td>
      <td>193</td>
      <td>1</td>
      <td>1</td>
      <td>141</td>
      <td>0</td>
      <td>3.4</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>0</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>301</th>
      <td>57</td>
      <td>1</td>
      <td>0</td>
      <td>130</td>
      <td>131</td>
      <td>0</td>
      <td>1</td>
      <td>115</td>
      <td>1</td>
      <td>1.2</td>
      <td>1</td>
      <td>1</td>
      <td>3</td>
      <td>0</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>302</th>
      <td>57</td>
      <td>0</td>
      <td>1</td>
      <td>130</td>
      <td>236</td>
      <td>0</td>
      <td>0</td>
      <td>174</td>
      <td>0</td>
      <td>0.0</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>0</td>
      <td>pass</td>
    </tr>
  </tbody>
</table>
<p>303 rows × 15 columns</p>
</div>




```python
df1[(df1["age"] >= 60 ) | (df1["sex"]==1)] # 차이가 뭐지? 
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
      <th>age</th>
      <th>sex</th>
      <th>cp</th>
      <th>trestbps</th>
      <th>chol</th>
      <th>fbs</th>
      <th>restecg</th>
      <th>thalach</th>
      <th>exang</th>
      <th>oldpeak</th>
      <th>slope</th>
      <th>ca</th>
      <th>thal</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>63</td>
      <td>1</td>
      <td>3</td>
      <td>145</td>
      <td>233</td>
      <td>1</td>
      <td>0</td>
      <td>150</td>
      <td>0</td>
      <td>2.3</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>37</td>
      <td>1</td>
      <td>2</td>
      <td>130</td>
      <td>250</td>
      <td>0</td>
      <td>1</td>
      <td>187</td>
      <td>0</td>
      <td>3.5</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>56</td>
      <td>1</td>
      <td>1</td>
      <td>120</td>
      <td>236</td>
      <td>0</td>
      <td>1</td>
      <td>178</td>
      <td>0</td>
      <td>0.8</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>57</td>
      <td>1</td>
      <td>0</td>
      <td>140</td>
      <td>192</td>
      <td>0</td>
      <td>1</td>
      <td>148</td>
      <td>0</td>
      <td>0.4</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>44</td>
      <td>1</td>
      <td>1</td>
      <td>120</td>
      <td>263</td>
      <td>0</td>
      <td>1</td>
      <td>173</td>
      <td>0</td>
      <td>0.0</td>
      <td>2</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>296</th>
      <td>63</td>
      <td>0</td>
      <td>0</td>
      <td>124</td>
      <td>197</td>
      <td>0</td>
      <td>1</td>
      <td>136</td>
      <td>1</td>
      <td>0.0</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>297</th>
      <td>59</td>
      <td>1</td>
      <td>0</td>
      <td>164</td>
      <td>176</td>
      <td>1</td>
      <td>0</td>
      <td>90</td>
      <td>0</td>
      <td>1.0</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>299</th>
      <td>45</td>
      <td>1</td>
      <td>3</td>
      <td>110</td>
      <td>264</td>
      <td>0</td>
      <td>1</td>
      <td>132</td>
      <td>0</td>
      <td>1.2</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>300</th>
      <td>68</td>
      <td>1</td>
      <td>0</td>
      <td>144</td>
      <td>193</td>
      <td>1</td>
      <td>1</td>
      <td>141</td>
      <td>0</td>
      <td>3.4</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>301</th>
      <td>57</td>
      <td>1</td>
      <td>0</td>
      <td>130</td>
      <td>131</td>
      <td>0</td>
      <td>1</td>
      <td>115</td>
      <td>1</td>
      <td>1.2</td>
      <td>1</td>
      <td>1</td>
      <td>3</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>245 rows × 14 columns</p>
</div>



20. Replacing Data


```python
df_mean.replace(56.786, "bad") # 한가지 데이터를 다른 한가지로 대체할 수 있다.
df_mean.replace([56.786,45.575],"bad") # 두개의 데이터를 다른 한가지로 대체할 수 있다. 오직 DataFrame에서만 가능. 문자열에서는 리스트값을 replace에 사용불가
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
      <th>class1</th>
      <th>class2</th>
      <th>class3</th>
      <th>class4</th>
      <th>class5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>78.567</td>
      <td>bad</td>
      <td>bad</td>
      <td>78.435</td>
      <td>78.435</td>
    </tr>
    <tr>
      <th>1</th>
      <td>67.545</td>
      <td>78.546</td>
      <td>69.564</td>
      <td>89.345</td>
      <td>89.345</td>
    </tr>
    <tr>
      <th>2</th>
      <td>89.565</td>
      <td>98.567</td>
      <td>59.342</td>
      <td>45.546</td>
      <td>45.546</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_new["sex"] = df1["sex"].replace([0,1],["male","female"]) # 여러개의 데이터를 짝을 지어 다른 여러개의 데이터로 대체할 수 있다.

print(df1)
```

         age  sex  cp  trestbps  chol  ...  slope  ca  thal  target  survived
    0     63    1   3       145   233  ...      0   0     1       1      fail
    1     37    1   2       130   250  ...      0   0     2       1      pass
    2     41    0   1       130   204  ...      2   0     2       1      pass
    3     56    1   1       120   236  ...      2   0     2       1      pass
    4     57    0   0       120   354  ...      2   0     2       1      pass
    ..   ...  ...  ..       ...   ...  ...    ...  ..   ...     ...       ...
    298   57    0   0       140   241  ...      1   0     3       0      pass
    299   45    1   3       110   264  ...      1   0     3       0      pass
    300   68    1   0       144   193  ...      1   2     3       0      fail
    301   57    1   0       130   131  ...      1   1     3       0      pass
    302   57    0   1       130   236  ...      1   1     2       0      pass
    
    [303 rows x 15 columns]


21. Handling Missing Value

* Missing Value 
* 데이터의 수집이 불가능하여 데이터가 없는 상태
* 빈칸, ?, 혹은 NaN등의 기호로 표기
* 에러나 오차를 발생시킬 수 있으므로 처리가 필요


```python
df.isna().any() # DataFrame의 각 열에서 결측값 유무 확인. 있으면 True
```




    a    False
    b    False
    c    False
    dtype: bool




```python
df.isna().sum() # DataFrame의 각 열에서 결측값의 갯수 확인. True는 1로 계산
df.isna().sum().sum() # DataFrame 전체에서 결측값의 갯수 확인.
```




    0




```python
df.isna().mean() # DataFrame에서 결측값의 비율 확인. True는 1로 계산
```




    a    0.0
    b    0.0
    c    0.0
    dtype: float64




```python
df.dropna() # 결측값이 포함된 행을 삭제
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
      <th>a</th>
      <th>b</th>
      <th>c</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>23</td>
      <td>45</td>
      <td>25</td>
    </tr>
    <tr>
      <th>1</th>
      <td>23</td>
      <td>67</td>
      <td>34</td>
    </tr>
    <tr>
      <th>2</th>
      <td>67</td>
      <td>46</td>
      <td>87</td>
    </tr>
  </tbody>
</table>
</div>




```python
#df.fillna(Value) # 결측값을 특정 값으로 채우기
# value = df.mean() - 결측값을 평균으로 채우기
# value = df.min() or max() - 결측값을 최솟값이나 최댓값으로 채우기
# value = method="ffill" - 결측값을 위값으로 채우기
# value = method="bfill" - 결측값을 아래값으로 채우기
df.fillna(method="ffill").fillna(method="bfill") # 0번 행의 값이 결측값일 경우에는 method="ffill" 사용할 수 없으므로 연달아 쓰는 경우가 많다.
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
      <th>a</th>
      <th>b</th>
      <th>c</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>23</td>
      <td>45</td>
      <td>25</td>
    </tr>
    <tr>
      <th>1</th>
      <td>23</td>
      <td>67</td>
      <td>34</td>
    </tr>
    <tr>
      <th>2</th>
      <td>67</td>
      <td>46</td>
      <td>87</td>
    </tr>
  </tbody>
</table>
</div>



22. Time Series Data(시계열 데이터 다루기)

* Time Series Data : 수집된 자료가 시간적 순서를 가지는 데이터
* 시계열 예측 : 과거의 데이터를 분석하여 미래의 상황 예측
* 시간 정보는 매출, 교통량, 주가, 과학적 실험 결과, 트렌드, 날씨, 이상 탐지 등의 예측에 자주 사용된다. 
* 과거의 데이터를 분석해 의사결정을 내리고 미래에 더 좋은 결과를 가져오기 위함. 
* 우리 눈에는 날짜처럼 보이지만 컴퓨터는 datetime 객체로 바꾸기 전까지는 단순한 문자열로 인식한다. 


```python
# 날짜 문자열을 datetime 객체로 바꾸기
import datetime as dt
df3 = pd.read_csv("Time.csv")
df3["date"] = pd.to_datetime(df3["date"]) # pd.to_datetime() 함수를 사용하면 날짜형식의 문자열을 datetime 객체로 변환한다.

print(df3.head())
```

            date  time  test  negative  confirmed  released  deceased
    0 2020-01-20    16     1         0          1         0         0
    1 2020-01-21    16     1         0          1         0         0
    2 2020-01-22    16     4         3          1         0         0
    3 2020-01-23    16    22        21          1         0         0
    4 2020-01-24    16    27        25          2         0         0



```python
df3["date"].dt.hour # 변환된 datetime 객체에는 datetime module의 기능을 사용할 수 있다.
df3["date"].dt.weekday 
```




    0      0
    1      1
    2      2
    3      3
    4      4
          ..
    158    4
    159    5
    160    6
    161    0
    162    1
    Name: date, Length: 163, dtype: int64



23. Data Binning(연속형 데이터 - 이산형 데이터)

* 연속적데이터(실수) - 범주형데이터(이산형데이터;정수)
* Ex) 몸무게의 경우 연속적인 데이터지만 이를 범주형데이터로 변환할 수 있다
* 이를 사용하는 이유는 인간의 관점에서는 데이터에 대한 더 쉬운 이해가 목적이고 기계의 관점에서는 머신러닝에서 더 좋은 결과값을 나타내는 경우가 많기 때문이다.


```python
df1["age"] = pd.cut(df1["age"], bins=4, labels=[0,1,2,3]) 
# pd.cut(series, bins=int, labels=[])를 사용하면 데이터의 유무와 상관없이 같은 크기의 int개의 구간으로 데이터들이 나뉨.

print(df1)
```

        age  sex  cp  trestbps  chol  ...  slope  ca  thal  target  survived
    0     2    1   3       145   233  ...      0   0     1       1      fail
    1     0    1   2       130   250  ...      0   0     2       1      pass
    2     0    0   1       130   204  ...      2   0     2       1      pass
    3     2    1   1       120   236  ...      2   0     2       1      pass
    4     2    0   0       120   354  ...      2   0     2       1      pass
    ..   ..  ...  ..       ...   ...  ...    ...  ..   ...     ...       ...
    298   2    0   0       140   241  ...      1   0     3       0      pass
    299   1    1   3       110   264  ...      1   0     3       0      pass
    300   3    1   0       144   193  ...      1   2     3       0      fail
    301   2    1   0       130   131  ...      1   1     3       0      pass
    302   2    0   1       130   236  ...      1   1     2       0      pass
    
    [303 rows x 15 columns]



```python
# 각 bins의의 빈도를 알기위해서는 groupby()와 count() 함수 이용하기.
df1.groupby("age", as_index=False).count()
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
      <th>age</th>
      <th>sex</th>
      <th>cp</th>
      <th>trestbps</th>
      <th>chol</th>
      <th>fbs</th>
      <th>restecg</th>
      <th>thalach</th>
      <th>exang</th>
      <th>oldpeak</th>
      <th>slope</th>
      <th>ca</th>
      <th>thal</th>
      <th>target</th>
      <th>survived</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
      <td>29</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
      <td>99</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
      <td>142</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
      <td>33</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2["math score"] =pd.qcut(df2["math score"], q=[0,0.25,0.5,0.75,1], labels=[0,1,2,3])
# pd.qcut(series, q=[], labels=[])를 사용하면 데이터가 작은 수부터 q에서 지정한 비율만큼 나뉜다. 사분위수 개념과 비슷함.

print(df2)
```

         gender race/ethnicity  ... reading score writing score
    0    female        group B  ...            72            74
    1    female        group C  ...            90            88
    2    female        group B  ...            95            93
    3      male        group A  ...            57            44
    4      male        group C  ...            78            75
    ..      ...            ...  ...           ...           ...
    995  female        group E  ...            99            95
    996    male        group C  ...            55            55
    997  female        group C  ...            71            65
    998  female        group D  ...            78            77
    999  female        group D  ...            86            86
    
    [1000 rows x 8 columns]



```python
# 각 bins의의 빈도를 알기위해서는 groupby()와 count() 함수 이용하기.
df2.groupby("math score",as_index=False).count()
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
      <th>math score</th>
      <th>gender</th>
      <th>race/ethnicity</th>
      <th>parental level of education</th>
      <th>lunch</th>
      <th>test preparation course</th>
      <th>reading score</th>
      <th>writing score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>266</td>
      <td>266</td>
      <td>266</td>
      <td>266</td>
      <td>266</td>
      <td>266</td>
      <td>266</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>241</td>
      <td>241</td>
      <td>241</td>
      <td>241</td>
      <td>241</td>
      <td>241</td>
      <td>241</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>264</td>
      <td>264</td>
      <td>264</td>
      <td>264</td>
      <td>264</td>
      <td>264</td>
      <td>264</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>229</td>
      <td>229</td>
      <td>229</td>
      <td>229</td>
      <td>229</td>
      <td>229</td>
      <td>229</td>
    </tr>
  </tbody>
</table>
</div>



24. One-hot Encoding & Label Encoding

* 문자열처럼럼 컴퓨터가 이해하기 어려운 데이터를 숫자로 표현
* 데이터 처리, 머신러닝, 자연어 처리를 하기 위한 가장 기초적인 표현방식
* 순서형 자료는 Label Encoding, 명목자료는 One-hot Encoding이 적합


```python
A_list = {"dept" : ["응용통계학과", "노어노문학과", "경영학과"]}
df4 = pd.DataFrame(A_list)

df4
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
      <th>dept</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>응용통계학과</td>
    </tr>
    <tr>
      <th>1</th>
      <td>노어노문학과</td>
    </tr>
    <tr>
      <th>2</th>
      <td>경영학과</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.get_dummies(df4) # pandas의 get_dummies 함수를 사용하면 one-hot encoding 가능
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
      <th>dept_경영학과</th>
      <th>dept_노어노문학과</th>
      <th>dept_응용통계학과</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2["gender"] = df2["gender"].map({"female" : 1, "male" : 0}) # .map({"name1" : value1, "name2" : value2})의 형식으로 label encoding 가능

df2
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
      <th>gender</th>
      <th>race/ethnicity</th>
      <th>parental level of education</th>
      <th>lunch</th>
      <th>test preparation course</th>
      <th>math score</th>
      <th>reading score</th>
      <th>writing score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>group B</td>
      <td>bachelor's degree</td>
      <td>standard</td>
      <td>none</td>
      <td>2</td>
      <td>72</td>
      <td>74</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>group C</td>
      <td>some college</td>
      <td>standard</td>
      <td>completed</td>
      <td>2</td>
      <td>90</td>
      <td>88</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>group B</td>
      <td>master's degree</td>
      <td>standard</td>
      <td>none</td>
      <td>3</td>
      <td>95</td>
      <td>93</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>group A</td>
      <td>associate's degree</td>
      <td>free/reduced</td>
      <td>none</td>
      <td>0</td>
      <td>57</td>
      <td>44</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>group C</td>
      <td>some college</td>
      <td>standard</td>
      <td>none</td>
      <td>2</td>
      <td>78</td>
      <td>75</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>995</th>
      <td>1</td>
      <td>group E</td>
      <td>master's degree</td>
      <td>standard</td>
      <td>completed</td>
      <td>3</td>
      <td>99</td>
      <td>95</td>
    </tr>
    <tr>
      <th>996</th>
      <td>0</td>
      <td>group C</td>
      <td>high school</td>
      <td>free/reduced</td>
      <td>none</td>
      <td>1</td>
      <td>55</td>
      <td>55</td>
    </tr>
    <tr>
      <th>997</th>
      <td>1</td>
      <td>group C</td>
      <td>high school</td>
      <td>free/reduced</td>
      <td>completed</td>
      <td>1</td>
      <td>71</td>
      <td>65</td>
    </tr>
    <tr>
      <th>998</th>
      <td>1</td>
      <td>group D</td>
      <td>some college</td>
      <td>standard</td>
      <td>completed</td>
      <td>2</td>
      <td>78</td>
      <td>77</td>
    </tr>
    <tr>
      <th>999</th>
      <td>1</td>
      <td>group D</td>
      <td>some college</td>
      <td>free/reduced</td>
      <td>none</td>
      <td>2</td>
      <td>86</td>
      <td>86</td>
    </tr>
  </tbody>
</table>
<p>1000 rows × 8 columns</p>
</div>

