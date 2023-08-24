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
버전 : 1.19.5 <br>
사용방법 : 다차원 배열 및 수학적 연산을 위한 라이브러리 <br>
<br>
``` 
import numpy as np
data = np.array([1, 2, 3])
print(data)
```

### 2-2 ) pandas  
설치 :  ``` !pip install pandas ```<br>
버전 : 1.3.3
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
### 2-5 ) warnings :
설치 : 

### 2-6 )

