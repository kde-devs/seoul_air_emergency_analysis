# Seoul PM2.5 and Emergency Room Visit Time-Series Analysis (2020-2021)
서울시 미세먼지와 응급실 방문 수 시계열 분석 (2020~2021)

# Overview | 개요
This project explores the time-series correlation between PM2.5 levels and emergency room visits in Seoul from 2020 to 2021
서울시의 미세먼지(PM2.5) 농도와 응급실 방문 수 사이의 시계열적 상관관게를 분석한 프로젝트입니다.

⚠️ This project was originally assigned as a team project. However, due to limited team participation, all data collection, processing, analysis, visualization, and documentation were independently completed by myself.

# Data Source | 데이터 출처
- **서울시 초미세먼지(PM2.5) 월별 농도**
  - 출처: [서울시 대기환경정보 월별 통계](https://cleanair.seoul.go.kr/statistics/monthAverage)
  - 설명: 서울시 측정소 기준, 월별 평균 PM2.5 농도 (2020–2021)

- **전국 대기오염 통합 데이터 (일별도 포함)**
  - 출처: [공공데이터포털 – 대기오염측정정보 API](https://www.data.go.kr/tcs/dss/selectApiDataDetailView.do?publicDataPk=15073861)
  - 설명: PM10, PM2.5 등 항목별 일별/시간별 측정 정보 제공 (Open API 가능)

- **서울시 응급실 이용자 수 (일별/자치구별)**
  - 출처: [서울열린데이터광장 – 응급실 이용자 현황](https://data.seoul.go.kr/dataList/11034/L/2/datasetView.do)
  - 설명: 서울시 자치구별 일자별 응급실 방문자 수 → 서울 전체 기준으로 합산 예정
# Methods | 분석 방법
- Time-series alignment & smoothing
- Lag correlation analysis
- Seasonal trend decomposition

# Key Findings | 주요 결과
- A strong correlation was observed with a 1-day lag between PM2.5 peaks and emergency visits.
- Seasonal patterns showed higher ER visits during winter with elevated dust levels

# Tech Stack | 기술 스택
- Python, Pandas, Matplotlib, Seaborn, Statsmodels
 
# File Structure | 파일 구성

