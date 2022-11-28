# 😊 today-score-project
## 💡 프로젝트 소개

#### 문제 상황

- 저희는 한국정보화진흥원(NIA)에서 주관하는 '데이터 분석가 양성 과정' 데잇걸즈 6기 수강생들 5명으로  구성된 팀입니다.
- 매일 교육 시작 전, 구글스프레드시트 출석부에 `오늘 나의 점수`를 작성하는데요. `오늘 나의 점수` 에 어떤 변수가 영향을 미칠지 궁금해서 프로젝트를 시작하게 됐습니다.

#### 프로젝트 목적

- `오늘 나의 점수`란 곧 오늘 나의 컨디션이라고 할 수 있습니다. 어떤 변수를 관리해야 최고의 컨디션으로 하루를 시작할 수 있을까요?

<br><br/>
## 📢 프로젝트 주제
- ****`오늘 나의 점수`를 높게 시작하려면 어떻게 해야 할까?****

<br><br/>
## 🗂 데이터 소개 
### 데이터 수집 개요
-  일자 : 2022-09-28 ~ 2022-11-14 (48일)
-  데이터 개수: 240 records
-  그라운드룰 : 매일 일어나서 최소 3시간 이내 구글스프레드시트에 평가합니다. 
※최소 3시간 이내 기준을 정한 이유 : 오늘 나의 점수를 매기는 것이기 때문에 일어나서 바로 평가하기 위해 기준을 정했습니다. (예시 : 7시 기상 시 10시 전에 평가)

### 데이터 수집 기준
<img width="70%" src = "https://user-images.githubusercontent.com/45919197/202838316-a2801f6d-1fba-4db5-b27c-cbfd16daa5be.png">


<br><br/>
## 📊 데이터 분석
### 데이터 분석 방법 
- Python이용한 ols 다중 회귀분석 진행 (P-value가 0.05보다 작은 변수 제외)

### 데이터 분석 결과
#### 1. 전체 (쿼카 + 공작 + 치타 + 토끼 + 다람쥐)
- 분석 결과   
  : 오늘 나의 점수를 높게 시작하기 위해서는 전날 누가 업어가도 모를 정도로 충분한 시간 동안 푹 잘 자고, 본인이 만족하는 하루를 보내야한다. 다른 변수는 큰 영향이 없다.
  ![image](https://user-images.githubusercontent.com/45919197/204278774-cc4cd43d-aedd-4b7b-a96b-f2fc9b3c6eac.png)
- 관련 파일 
  - [today_score_data](https://github.com/today-score-project/tsp/blob/main/rawdata/today_score_data.xlsx)
  - [all_today_score_project](https://github.com/today-score-project/tsp/blob/main/data_analysis/all_today_score_project.ipynb)

#### 2. 쿼카 
  - 분석 결과   
    : 쿼카가 오늘 나의 점수를 높게 시작하려면, 전날을 잘 보내고 잘 자야 한다. 다른 변수는 큰 영향이 없다. 많이 걷는 것은 전날의 만족도에 약간의 영향이 있다.
  ![image](https://user-images.githubusercontent.com/45919197/204278908-02fc8a3f-4f47-492b-be2e-b6769df32d40.png)
  - 관련 파일 : [quokka_today_score_project](https://github.com/today-score-project/tsp/blob/main/data_analysis/quokka_today_score_project.ipynb)
#### 3. 공작
  - 분석 결과   
    : 공작이 오늘 나의 점수를 높게 시작하기 위해서는 전날 만족스러운 하루를 보내야 한다. 다른 변수는 큰 영향이 없다. 만족스러운 하루를 보내는 데에는 많이 걷고 잘 자는 게 도움이 된다
  ![image](https://user-images.githubusercontent.com/45919197/204278964-33c44d46-9a67-410b-bc29-cc2c0b95e92a.png)
  - 추가 해석 (전날 하루 만족도를 종속변수로 추가 분석 진행)  
    : 만족스러운 하루를 보내는 데에는 많이 걷고 잘 자는 게 도움이 된다.
   ![image](https://user-images.githubusercontent.com/45919197/204279089-c17f67c7-46c7-495f-8a92-aca565827ec1.png)
  - 관련 파일 : [peacock_today_score_project](https://github.com/today-score-project/tsp/blob/main/data_analysis/peacock_today_score_project.ipynb)
#### 4. 치타
  - 분석 결과  
    : 치타가 오늘 나의 점수를 높게 시작하기 위해서는 잠이 제일 중요하다. 오전 2시 이전에 자야하고, 누가 업어가도 모를 정도로 푹 잘 자야한다. 다른 변수는 큰 영향이 없다.
    ![image](https://user-images.githubusercontent.com/45919197/204280455-113c4b91-ee0a-4779-8b83-ea23701becd1.png)
  - 관련 파일 : [cheetah_today_score_project](https://github.com/today-score-project/tsp/blob/main/data_analysis/cheetah_today_score_project.ipynb)
#### 5. 토끼
  - 분석 결과  
    : 토끼가 오늘 나의 점수를 높게 시작하려면, 수면점수, 어제 만족도를 높여야 한다. 전 날의 행동들이 다음 날의 점수에 큰 영향을 미치는 만큼, 수면점수와 어제 만족도를 높이기 위한 외부 변수들도 종합적으로  고려해 볼 필요가 있다.
  ![image](https://user-images.githubusercontent.com/45919197/204280892-b135040b-2369-4e7a-b24d-c3853d6f6bf3.png)  
  - 관련 파일 : [rabbit_today_score_project](https://github.com/today-score-project/tsp/blob/main/data_analysis/rabbit_today_score_project.ipynb)
#### 6. 다람쥐 
  - 분석 결과  
    : 다람쥐가 오늘 나의 점수를 높게 시작하기 위해서는 전날 만족도가 높은 하루를 마무리해야하고, 잠을 많이 자야한다. 
  ![image](https://user-images.githubusercontent.com/45919197/204281184-fa7af6c4-2f69-4938-a154-6d2073fad959.png)
  - 관련 파일 : [squirrel_today_score_project](https://github.com/today-score-project/tsp/blob/main/data_analysis/squirrel_today_score_project.ipynb)

<br><br/>
## 👋 팀 소개
* 김남이| Data Analyst : monamienamie@gmail.com
* 김민지| Data Analyst : dallaemin.kim@gmail.com
* 김혜원| Data Analyst : hyeweon.kym@gmail.com
* 김효진| Data Analyst : gywls630010@gmail.com
* 장회정| Data Analyst : hoinnovation@naver.com
