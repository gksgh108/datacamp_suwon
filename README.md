## 프로젝트 : 주가 데이터를 활용한 일/주/월 모델 통합 인공지능 모델링 분석

- 기간 : 2023.08.07 ~ 2023.08.27
- 팀원 : 이승연, 임소연, 임형섭, 곽병찬, 김한호
- 분석 도구 : Python

***

## 1. 프로젝트 개요
### 1-1 ) 프로젝트 목적
- 

### 1-2 ) 프로젝트 필요성 

***

## 2. 라이브러리  
### 2-1 ) numpy
설치 : ``` !pip install numpy ```<br>
버전 : 1.24.3 <br>
사용방법 : 다차원 배열 및 수학적 연산을 위한 라이브러리 <br>

### 2-2 ) pandas  
설치 :  ``` !pip install pandas ```<br>
버전 : 2.0.3
사용방법 : 데이터 조작 및 분석을 위한 라이브러리

### 2-3 ) tdqm
설치 :  ``` !pip install tqdm ```<br>
버전 : 4.64.1
사용방법 : 진행 상황을 표시하는 라이브러리

### 2-4 )  datetime
설치: 파이썬의 내장 라이브러리이므로 별도 설치 없이 사용 가능
사용방법 : 날짜와 시간 처리를 위한 라이브러리

### 2-5 )  warning
설치: 파이썬의 내장 라이브러리이므로 별도 설치 없이 사용 가능
사용방법 : 경고 메시지 관리를 위한 라이브러리

### 2-6 )  pykrx
설치: ``` !pip install pykrx ``` <br>
버전 : 1.0.45
사용방법 : 한국 주식 시장 데이터 조회를 위한 라이브러리

### 2-7 )  ta
설치: ``` !conda install -c conda-forge ta ``` <br>
버전 : 0.10.2
사용방법 : 다양한 기술적 지표를 계산하여 주가 데이터와 관련된 정보를 얻을 수 있는 라이브러리

### 2-8 ) matplotlib
설치: ``` !pip install matplotlib ``` <br>
버전 : 3.6.2
사용방법 : 데이터 시각화를 위한 라이브러리

### 2-9 ) seaborn 
설치: ``` !pip install seaborn ``` <br>
버전 : 0.12.2
사용방법 : Matplotlib을 기반으로 한 고급 데이터 시각화 라이브러리

***

## 3. 코드 실행

### 3-1 ) EDA 

### 3-2 ) 데이터 구축
! 실행하기 전에 라이브러리 import 필수
#### 일별 raw 데이터
- 기본 데이터를 pykrx라이브러리를 이용해서 구축
  - 정보를 가져올 코스피 종목 가져오기 전부 실행 후 실행 (kospi200 = result_df['Symbol']까지)
  - 실행시간 약 50분 소요 -> 데이터 파일 따로 구글 드라이브로 공유
<img src="raw_data.png" width="800px" height="400px" title="기본데이터" alt="기본데이터"></img><br/>

#### 일별 보조지표 추가 데이터<br>
- 기본 데이터에 보조지표를 계산하여 추가
  - 보조지표 가져오기 함수 실행 후 일별 데이터 생성(보조지표 추가)를 실행
  - 후에 day_data.csv로 저장까지 실행
<img src="raw_data_index.png" width="800px" height="400px" title="일별 보조지표 데이터" alt="기본데이터"></img><br/>

#### 주별 데이터
- 일별 데이터를 기반으로 생성한 주별 데이터를 일별로 쌓이도록 한 뒤 이동평균선을 계산하여 추가
  - 함수로 만들어 WD(일별데이터)로 실행하면 결과값이 나옴
  - 결과값 중 필요한 date, Open, High,	Low,	Close,	Trading,	code만 저장하고 weekly로 칼럼명 변경
<img src="weekly_data.png" width="800px" height="400px" title="주별 데이터" alt="기본데이터"></img><br/>

#### 월별 데이터
- 일별 데이터를 기반으로 생성한 월별 데이터를 일별로 쌓이도록 한 뒤 이동평균선을 계산하여 추가
  - 함수로 만들어 MD(일별데이터)로 실행하면 결과값이 나옴
  - 결과값 중 필요한 date, Open, High,	Low,	Close,	Trading,	code만 저장하고 weekly로 칼럼명 변경
<img src="monthly_data.png" width="800px" height="400px" title="월별 데이터" alt="기본데이터"></img><br/>
