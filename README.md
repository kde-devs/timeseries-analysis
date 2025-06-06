# timeseries-Data Analysis Project

서울시의 미세먼지와 응급실 방문 수 사이의 시계열적 상관관계 분석 (2020~2021)
이 프로젝트는 서울시의 대기질(PM2.5)과 응급실 이용량 사이의 시계열적 상관관계를 분석하여 공공 보건 정책 수립에 기여하고자 합니다.

# Project Overview
분석 배경 : 산불과 미세먼지 등으로 대기질이 급격히 악화될 때, 응급실 방문자가 증가할 수 있다는 가설을 정량적으로 분석하고자 하였습니다.
연구 목적 : 서울시의 2020~2021년 월별 PM2.5 농도와 응급실 방문 수 데이터를 기반으로, 시계열 분석 및 예측을 통해 공공 보건 대응 전략, 건강경보 시스템 개선, 의료 자원 배분 전략에 실질적인 근거를 제시합니다.

# Data Sources
- 서울열린데이터광장 : 자치구별 월별 PM2.5 농도
- 응급의료 데이터 : 월별 응급실 방문 통계
- 기상청 Open API : 월별 평균기온, 최고/최저기온

# Tools & Techniques
- Python (Pandas, Matplotlib, Seaborn, Statsmodels)
- Time Series Modeling: SARIMA, SARIMAX
- Correlation Analysis: Pearson correlation with time lag (Lag 0 to 3 months)
- Scenario-Based Forecasting (e.g., PM +30%, PM –20%)

# Key Findings
- Heatmap analysis reveals moderate to strong correlation between PM2.5 levels and ER visits
- SARIMAX model forecasts monthly ER visit counts under different pollution scenarios
- In 2026 forecast:
  - Under PM +30 scenario → ER visits rise from ~170,000 (Jan) to ~880,000 (Dec)
  - Under PM –20 scenario → ER visits rise from ~130,000 (Jan) to ~460,000 (Dec)
  - ER visits surge in spring/summer and peak gap appears in winter

# Project Notebooks

#1 Preprocessing

- [자치구 미세먼지 전처리](https://github.com/kde-devs/timeseries-analysis/blob/main/notebooks/1_preprocessing/자치구_미세먼지_전처리.ipynb)
- [응급실 데이터 전처리](https://github.com/kde-devs/timeseries-analysis/blob/main/notebooks/1_preprocessing/응급실_데이터_전처리.ipynb)
- [기온데이터 전처리](https://github.com/kde-devs/timeseries-analysis/blob/main/notebooks/1_preprocessing/기온데이터_전처리.ipynb)

---

#2 Exploratory Data Analysis (EDA)

- [자치구별 미세먼지 시각화](https://github.com/kde-devs/timeseries-analysis/blob/main/notebooks/2_eda/자치구_별_미세먼지_시각화.ipynb)
- [응급실 데이터 시각화](https://github.com/kde-devs/timeseries-analysis/blob/main/notebooks/2_eda/응급실_데이터_시각화.ipynb)
- [기온데이터 시각화](https://github.com/kde-devs/timeseries-analysis/blob/main/notebooks/2_eda/기온데이터_시각화.ipynb)
- [단순 상관관계 분석](https://github.com/kde-devs/timeseries-analysis/blob/main/notebooks/2_eda/단순%20상관관계%20분석.ipynb)

---

#3 Time Series Forecasting

- [2026년 가상 시나리오 예측진행 (Base / PM+30 / PM–20)](https://github.com/kde-devs/timeseries-analysis/blob/main/notebooks/3_prediction/2026년%20가상%20시나리오%20예측진행%20(Base%20_%20PM%2B30%20_%20PM–20)%20.ipynb)

#  Expected Outcomes
- 사전 대응 강화 : 미세먼지 급등 시 ER 수요 예측 → 의료진 및 장비 선제 배치 가능
- 정책 근거 마련 : 미세먼지 경보 기준 재조정 및 대기질 개선 정책 설계에 기여
- 자원 배분 최적화 : 병원 간 환자 분산, 의약품 확보 계획 수립 등 지원

# Conclusion
본 프로젝트는 단기 환경 변화가 의료 수요에 미치는 영향을 시계열적으로 조명함으로써, 실제 정책 수립에 기여할 수 있는 데이터 기반 분석 사례를 제시합니다.
