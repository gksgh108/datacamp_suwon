## 프로젝트 : 주가 데이터를 활용한 일/주/월 모델 통합 인공지능 모델링 분석

- 기간 : 2023.08.07 ~ 2023.08.27
- 팀원 : 이승연, 임소연, 임형섭, 곽병찬, 김한호
- 분석 도구 : Python

## 1. 프로젝트 개요
### 1-1 ) 프로젝트 목적
- 

### 1-2 ) 프로젝트 필요성 

## 2. 라이브러리  
### 2-1 ) numpy
설치 : ``` !pip install numpy ```<br>
버전 : 1.24.3 <br>
사용방법 : 다차원 배열 및 수학적 연산을 위한 라이브러리 <br>
<br>
``` 
import numpy as np
data = np.array([1, 2, 3])
print(data)
```

### 2-2 ) pandas  
설치 :  ``` !pip install pandas ```<br>
버전 : 2.0.3
사용방법 : 데이터 조작 및 분석을 위한 라이브러리
``` 
import pandas as pd 
data = {'Name': ['Alice', 'Bob', 'Charlie'], 'Age': [25, 30, 22]} 
df = pd.DataFrame(data) 
print(df)
```

### 2-3 ) tdqm
설치 :  ```  !pip install tqdm ```<br>
버전 : 4.64.1
사용방법 : 진행 상황을 표시하는 라이브러리
``` 
from tqdm import tqdm
import time 
for _ in tqdm(range(10)):
time.sleep(0.1)
```

### 2-4 )  datetime
설치: 파이썬의 내장 라이브러리이므로 별도 설치 없이 사용 가능
사용방법 : 날짜와 시간 처리를 위한 라이브러리
``` 
import datetime 
current_time = datetime.datetime.now() 
print(current_time)
```

### 2-5 )  warning
설치: 파이썬의 내장 라이브러리이므로 별도 설치 없이 사용 가능
사용방법 : 경고 메시지 관리를 위한 라이브러리
``` 
import warnings 
warnings.warn("This is a warning message.")
``` 

### 2-6 )  pykrx
설치: ``` !pip install pykrx ``` <br>
버전 : 1.0.45
사용방법 : 한국 주식 시장 데이터 조회를 위한 라이브러리
```
from pykrx import stock 
df = stock.get_market_ohlcv_by_date("20230101", "20230105", "005930")
print(df)
```

### 2-7 )  ta
설치: ``` !conda install -c conda-forge ta ``` <br>
버전 : 0.10.2
사용방법 : 다양한 기술적 지표를 계산하여 주가 데이터와 관련된 정보를 얻을 수 있는 라이브러리
```
import pandas as pd
from ta import add_all_ta_features
from ta.utils import dropna

# Load datas
df = pd.read_csv('ta/tests/data/datas.csv', sep=',')

# Add all ta features
df = add_all_ta_features(
    df, open="Open", high="High", low="Low", close="Close", volume="Volume_BTC")
```

### 2-8 ) matplotlib
설치: ``` ! pip install matplotlib ``` <br>
버전 : 3.6.2
사용방법 : 데이터 시각화를 위한 라이브러리
```
import matplotlib.pyplot as plt 
x = [1, 2, 3, 4, 5] 
y = [10, 20, 15, 30, 25] 
plt.plot(x, y) plt.xlabel('X-axis') 
plt.ylabel('Y-axis') plt.title('Sample Plot') 
plt.show()
```

### 2-9 ) matplotlib
설치: ``` ! pip install matplotlib ``` <br>
버전 : 3.6.2
사용방법 : 데이터 시각화를 위한 라이브러리
```
import matplotlib.pyplot as plt 
x = [1, 2, 3, 4, 5] 
y = [10, 20, 15, 30, 25] 
plt.plot(x, y) plt.xlabel('X-axis') 
plt.ylabel('Y-axis') plt.title('Sample Plot') 
plt.show()
```

### 2-10 ) seaborn 
설치: ``` ! pip install seaborn ``` <br>
버전 : 0.12.2
사용방법 : Matplotlib을 기반으로 한 고급 데이터 시각화 라이브러리
```
import seaborn as sns

tips = sns.load_dataset("tips") 
sns.set(style="whitegrid") 
sns.boxplot(x="day", y="total_bill", data=tips) 
plt.xlabel('Day') plt.ylabel('Total Bill ($)') 
plt.title('Total Bill by Day') plt.show()
```

## 3. 코드 실행

### 3-1 ) 데이터 구축

####

![데이터 예시](raw_data.jpg)


