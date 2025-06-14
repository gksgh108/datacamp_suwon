## 프로젝트 : 주가 데이터를 활용한 일/주/월 모델 통합 인공지능 모델링 분석

- 팀원 : 이승연, 임소연, 임형섭, 곽병찬, 김한호
- 분석 도구 : Python

***

### 1. 제출파일
  1) Readme.md : 코드 실행 방법 설명
  2) code : 실행을 위한 코드
     1. [1] 데이터셋 구축 - 데이터를 일, 주, 월 데이터로 통합하는 과정
     2. [2] 모델 학습 - 통합된 데이터를 학습시키는 과정
     3. 참고용 - 주가 데이터를 가져온 경위 설명
  3) data : 실행을 위한 데이터
     1. code_list - 데이터를 가져오기 위한 코드명
     2. raw_data - 데이터를 가져온 첫 raw data
  4) model : 최적의 모델을 저장해둔 폴더

***

### 2. 데이터 획득방법
- 기본적으로 주가 공개 데이터를 사용한다
  - 데이터셋.ipynb 파일을 실행하면, 파이썬 pykrx 라이브러리를 통해서 주가 데이터를 다운로드 받고 raw_data.csv와 day_data, week_data, month_data, all_data를 저장한다.
  - 위의 방법으로 데이터 다운로드하면 시간이 오래걸리기 때문에, 최종 파일을 포함시킨다.

***

### 3. requirement -> 필요한 사전 설치 프로그램
  1) python
  2) jupyter notebook 혹은 jupyter lab
  3) 코드 실행에 필요한 파이썬 라이브러리
     - numpy
     - pandas
     - tdqm
     - datetime
     - warning
     - pykrx
     - ta
     - matplotlib
     - seaborn
     - tensorflow
     - keras_tuner
     - sklearn
  (기본적으로 설치되어있는 datetime과 warning을 제외하고 나머지는 설치할 수 있도록 코드를 짜놓음)

***

### 4. 실행방법
  case 1. pykrx라이브러리를 이용하여 전체 데이터를 다운로드 받아서 실행시키는 법(데이터 다운로드 시간이 오래걸림 -> 이 부분은 제외)
  1) 제출한 압축 파일의 압축을 푼다
  2) 작업폴더 안에 code폴더를 생성하여 받은 code파일(*.ipynb)을 code에 넣고 data폴더를 생성한다(csv파일들은 불필요)
  3) jupyter notebook이나 lab을 실행하고,
    - 1_데이터셋.ipynb를 보조지표 가져오기(Markdown) 전까지 실행한 후 2_EDA.ipynb를 실행하여 EDA 결과를 본다음 다시 돌아와 남은 데이터셋.ipynb를 전부 실행시킨다.
    - 3_모델링.ipynb에서 처음부터 실행시킨다.
   
  case 2. 제출한 데이터 파일을 사용하는 경우(데이터 다운로드 시간 절약 - pickle형태로 압축된 data사용)
  1) 제출한 압축 파일의 압축을 푼다.
  2) 작업폴더 안에 code폴더를 생성하여 받은 code파일(*.ipynb)을 code에 넣고 data폴더에 받은 데이터 파일(data.csv파일)이 위치한지 확인한다.
  3) jupyter noteboo이나 lab을 실행하고,
    - 바로 code의 [2] 모델 학습만 실행하여도 실행가능
