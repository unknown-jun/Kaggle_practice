# Porto Seguro's Safe Driver Prediction

- Data Structural Feature:

1. 운전자가 내년에 보험 청구를 할 것인지를 예측하는 것이 목적
2. 매우 불균형한 Target Label
3. 평가지표가 Normalized Gini Coefficient
4. 모든 Column들이 비식별화 처리가 되어 있음

- Data Feature: train- (595212, 59) / test- (892816, 58)

## 1. Data Preparation & Exploration

- Source: [Bert Carremans 커널](https://www.kaggle.com/bertcarremans/data-preparation-exploration)
- Special Feature:
1. 각 feature들의 특징을 담은 Meta Data를 만들어 활용
2. Categorical 변수의 Encoding 방식을 Mean Encoding을 적용한 것이 인상적
3. 데이터 불균형의 해결을 Undersampling을 사용함(데이터 사이즈가 매우 크기 때문)

