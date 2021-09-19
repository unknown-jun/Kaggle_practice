# Titanic
- Data Feature: train- (891, 12) / test- ( 418, 11)
- Feature Imformation
![image](https://user-images.githubusercontent.com/70187490/133928405-a44fb615-ef35-42ea-8a33-05a454cd86ae.png)

## 1. RandomForest / Pycaret
- Source: [캐글 코리아](https://kaggle-kr.tistory.com/17)

- Special Feature:
1. 'Name' Column을 정규 표현식으로 추출하여 Initial이라는 파생변수 생성
2. 앞서 생성한 Initial을 근거로 'Age'의 결측치를 예측함

- Modeling:
1. RandomForest의 하이퍼 파라미터를 GridSearch를 이용해 최적의 정확도를 찾으려 노력
2. Pycaret이라는 라이브러리를 사용해 최적의 Model을 도출

## 2. Voting
- Source: [안드레이 룩야넨코 한글 번역 커널](https://www.kaggle.com/joshuajhchoi/titanic-tutorial-for-beginners-2020)

- Special Feature:
1. pd.crosstab을 이용해 각 value의 빈도수를 추출한 점이 인상적이었음
2. 여러 변수의 조건을 주어 생존률이 높은 특징을 찾아내 파생변수만으로 테이블을 생성한 Column Selection
3. train 파일과 test 파일을 concat시켜 한번에 Feature Engineering

- Modeling:
1. 11개의 모델에서 각각 GridSearch를 실시해 최적의 하이퍼 파라미터를 도출한 뒤
2. Voting으로 최종 결과를 만듦
