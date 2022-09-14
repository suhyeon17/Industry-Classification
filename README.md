# 통계데이터 인공지능 활용대회 
https://data.kostat.go.kr/sbchome/contents/cntPage.do?cntntsId=CNTS_000000000000575&curMenuNo=OPT_09_03_00_0


### 목표
자연어 기반 산업분류 자동화 인공지능 모델 개발
- 자연어 기반의 통계 데이터를 인공지능으로 자동 분류하는 모델 발굴

### 데이터
- X: text_obj = 사업 대상 , text_mthd = 사업 방법, text_deal = 사업 취급품목  
- y: digit_1 = 대분류, digit_2=중분류, digit_3=소분류

### 성능 평가
- 부분 점수: 대분류 예측(0.1점), 중분류 예측(0.2점), 소분류 예측(0.7점)
- Accuracy: 정확히 분류된 표본 / 전체 표본
- F1-Score: 각 산업분류 카테고리별 F1-Score를 산술평균으로 계산하여 최종 F1-Score 산출

### BiLSTM(양방향 LSTM)
- BiLSTM: 두 개의 독립적인 LSTM 아키텍쳐를 함께 사용
- 자연어 Task에서 문장을 왼쪽 단어부터 순차적으로 읽는 **순방향 LSTM**과 뒤의 문맥을 고려하기 위해 오른쪽 부터 반대로 읽는 **역방향 LSTM**을 함께 사용  
  
  
![image](https://user-images.githubusercontent.com/77714083/190184181-85369300-e725-425d-86b1-e7fd013ef4b4.png)
[출처] https://yeong-jin-data-blog.tistory.com/entry/LSTM?category=993409

