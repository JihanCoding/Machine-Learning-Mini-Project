
# 학생 성적 예측 머신러닝 미니 프로젝트

이 프로젝트는 학생 성적에 영향을 미치는 다양한 요인을 분석하고, 이를 기반으로 성적을 예측하는 머신러닝 모델을 구축하는 것을 목표로 합니다. 주요 목표는 성적 예측을 통해 학생 개별화 학습 계획을 지원하는 것입니다.

## 1. 프로젝트 개요
- **목적**: 학생 성적에 영향을 미치는 요인을 분석하여 성적을 예측하고, 이 정보를 바탕으로 학생 개별화 학습 계획을 지원합니다.
- **데이터 출처**: 학생들의 학습 관련 변수들을 포함하는 데이터를 사용하였습니다.
- **사용된 알고리즘**: 선형 회귀(Linear Regression), 랜덤 포레스트 회귀(Random Forest Regressor)

## 2. 데이터셋 설명
데이터셋은 학생 성적에 영향을 미칠 수 있는 여러 특성들로 이루어져 있습니다. 주요 변수들은 다음과 같습니다:

- **Hours_Studied**: 주당 학습 시간
- **Attendance**: 출석률
- **Parental_Involvement**: 부모의 학습 참여도
- **Access_to_Resources**: 학습 자원 접근성
- **Extracurricular_Activities**: 방과 후 활동 참여 여부
- **Sleep_Hours**: 수면 시간
- **Previous_Scores**: 이전 시험 점수
- **Motivation_Level**: 학습 동기 수준
- **Internet_Access**: 인터넷 접근성
- **Tutoring_Sessions**: 과외 횟수
- **Family_Income**: 가정 소득 수준
- **Teacher_Quality**: 교사 평가
- **School_Type**: 학교 유형
- **Physical_Activity**: 신체 활동 정도
- **Learning_Disabilities**: 학습 장애 여부
- **Parental_Education_Level**: 부모의 교육 수준
- **Distance_from_Home**: 학교와의 거리
- **Gender**: 성별
- **Exam_Score**: 시험 점수 (타겟 변수)

## 3. 데이터 전처리
- **결측치 처리**: 결측치가 있는 경우 평균값으로 대체하거나, 해당 데이터를 제거하였습니다.
- **범주형 변수 인코딩**: `Parental_Education_Level`, `School_Type` 등의 범주형 변수는 One-Hot Encoding을 사용해 처리하였습니다.
- **특성 스케일링**: `Hours_Studied`, `Attendance`와 같은 연속형 변수는 StandardScaler를 사용해 정규화하였습니다.

## 4. 모델 구축
학생 성적을 예측하기 위해 두 가지 모델을 실험했습니다.

- **RandomForestRegressor** (랜덤 포레스트 회귀)
- **GradientBoostingRegressor** (그레디언트 부스팅 회귀)
- **XGBRegressor** (XGBoost 회귀)
- **LinearRegression** (선형 회귀)
- **LGBMRegressor** (LightGBM 회귀)

## 5. 모델 평가
- **평가 지표**: 평균 제곱 오차(MSE)와 결정계수(R²)를 사용하여 모델의 성능을 평가하였습니다.
- **결과**: 선형 회귀 모델이 제일 높은 R² 값을 기록하며 비교적 정확한 예측을 제공하였습니다.

## 6. 결론
학생 성적에 영향을 미치는 요인으로는 **학습 시간**, **부모의 학력 수준**, **출석률** 등이 큰 영향을 미치는 것으로 나타났습니다. 특히 선형 회귀 모델을 통해 선형적인 관계를 잘 포착할 수 있었습니다.
