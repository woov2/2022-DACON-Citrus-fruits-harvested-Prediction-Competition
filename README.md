# 2022 DACON Citrus fruits harvested Prediction Competition
### 감귤 착과량 예측 AI 개발

## 1. 배경 & 목적

- 감귤의 생산량 추정은 수확 후 관리와 마케팅 계획 그리고 더 나아가 노동력 산출 및 저장 계획의 근거로 감귤 재배에 있어 필수 요소 중 하나임.
- 감귤 생산량 추정을 위한 한정된 조사인력이 약 22,000ha에 이르는 방대한 면적을 조사하기에, 시간이 오래 걸릴 뿐만 아니라 조사인력도 부족한 실정.
- 조사인력은 관측조사에 의존하기 때문에 일관되지 않은 데이터 수집이 이뤄지는 문제점.
- 감귤나무의 나무 생육 상태, 엽록소 및 새순 정보로부터 감귤 착과량을 정확히 예측할 수 있다면 위와 같은 문제를 모두 해결가능.
- 감귤의 생산량 추정에 도움을 줄 수 있는 감귤 착과량 예측 AI 모델 개발.
- 평가 지표: NMAE

<br/>

## 2. 주최/주관 & 참가 대상 & 성과

- 주최/주관: 제주 테크노파크 / DACON
- 참가 대상: 일반인, 학생 등 누구나
- 성과: 상위 6%

<br/>

## 3. 대회 기간

- 제출마감: 2022년 12월 14일
- 코드 평가 마감 및 최종순위 발표: 2022년 12월 16일

<br/>

## 4. 내용
- Target과의 correlation이 0.9보다 큰 Feature만 Selection
- Target의 상위 1%, 하위 1%를 이상치로 간주하여 clip
- 월별 새순 및 엽록소 데이터의 통계 Feature를 생성(mean, max, min, sum, diff, std, var, ...)
- Outlier 처리 및 표준화 진행
- SelectPercentile을 사용해 Feature Selection
- LGBM / XGB / Catboost를 사용해 Model Ensemble

<br/>

## 5. Process

### ch.1 Feature Engineering

- EDA
- Continuous Features Engineering(Statistic Method)

---

### ch.2 Preprocessing

- Feature Correlation
- Outlier Processing
- Standardization
- Feature Selection

---

### ch.3 Modeling

- LGBM
- XGBOOST
- CATBOOST

---

### ch.4 Ensemble

- Weighted Ensemble
- LGBM 4 : XGB 4 : CATBOOST 2

<br/>

## 6. 참고자료

[데이콘 감귤 착과 예측 AI 경진대회 사이트](https://dacon.io/competitions/official/236038/overview/description)
