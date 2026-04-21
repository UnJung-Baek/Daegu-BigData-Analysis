# 🚒 제7회 대구 빅데이터 분석 경진대회

> **대구시 소방차 출동로 취약지역 분석 및 머신러닝 기반 위험도 예측 및 정책 시뮬레이션**

---

## 🏆 대회 개요
- **대회명:** 제7회 대구 빅데이터 분석 경진대회  
- **주최:** 대구광역시 × 대구 빅데이터 활용센터  

### 📌 문제 정의
대구시 읍면동 단위에서 **화재 출동 도착시간과 출동횟수를 예측**하고,  
이를 기반으로 **출동로 취약지역을 도출 및 정책 개선 효과를 분석**하는 것을 목표로 합니다.

---

## 🎯 분석 접근

본 프로젝트는 단순 예측이 아닌 아래 3가지 흐름을 중심으로 설계했습니다.

- 어디가 위험한가 → **예측**
- 왜 위험한가 → **SHAP 해석**
- 무엇을 바꾸면 얼마나 개선되는가 → **정책 시뮬레이션**

---

## ⚙️ 실행 환경

| 항목 | 내용 |
|------|------|
| Python | 3.10 |
| 주요 라이브러리 | pandas, numpy, scikit-learn, xgboost, optuna, shap |

---

## 📂 데이터

### 🔹 특징
- 가공되지 않은 **RAW 데이터 제공**
- 센터 내 전처리 후 검수·반출 필요
- 부족한 데이터는 **공공 데이터 직접 수집**

### 🔹 활용 데이터
- 화재 출동 데이터 (시간 / 요일 / 월)
- 교통 데이터 (통행량, 속도)
- 도로 데이터 (도로폭, 길이)
- 인구 및 행정 데이터

---

## 📁 프로젝트 구조
```bash
project/
│
├── 분석모델 및 데이터/
│   ├── model.ipynb
│   ├── simulation.ipynb
│   ├── 대구통합정보.csv
│   │
│   └── 화재/
│       ├── 화재_시간.csv
│       ├── 화재_요일.csv
│       ├── 화재_월.csv
│       │
│       ├── fire_time_pred.csv
│       ├── fire_day_pred.csv
│       ├── fire_month_pred.csv
│       │
│       ├── fire_time_dong_top10_features.csv
│       ├── fire_day_dong_top10_features.csv
│       ├── fire_month_dong_top10_features.csv
│       │
│       ├── model_fire_time_count_hour.joblib
│       ├── model_fire_time_time_hour.joblib
│       ├── model_fire_day_count_day.joblib
│       ├── model_fire_day_time_day.joblib
│       ├── model_fire_month_count_month.joblib
│       ├── model_fire_month_time_month.joblib
│       │
│       └── sim_dasa_road_timehour.csv
│
├── 공공_애플살껄_분석보고서_HWP.hwp
├── 공공_애플살껄_분석보고서_HWP.pdf
├── 공공_애플살껄_분석보고서_PPT.pdf
│
├── README.md
└── .gitignore
```

---

