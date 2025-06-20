# Seoul PM2.5 and Emergency Room Visit Time-Series Analysis (2020-2021)
서울시 미세먼지와 응급실 방문 수 시계열 분석 (2020~2021)

# Overview | 개요
This project explores the time-series correlation between PM2.5 levels and emergency room visits in Seoul from 2020 to 2021
서울시의 미세먼지(PM2.5) 농도와 응급실 방문 수 사이의 시계열적 상관관게를 분석한 프로젝트입니다.

⚠️ This project was originally assigned as a team project. However, due to limited team participation, all data collection, processing, analysis, visualization, and documentation were independently completed by myself.

# Data Source | 데이터 출처
- **서울시 초미세먼지(PM2.5) 농도**
  - 출처: [서울특별시 대기환경정보 – 열린데이터광장](https://data.seoul.go.kr/dataList/OA-2212/S/1/datasetView.do)
  - 설명: 서울시 측정소 기준 일별 평균 PM2.5 농도 데이터 (2020–2021)

- **PM2.5 항목 정의 및 측정 기준**
  - 출처: [한국환경공단 – 에어코리아](https://www.airkorea.or.kr/web/detailViewDown?pMENU_NO=125)
  - 설명: PM2.5 항목 정의, 측정방법, 장비 정보 등 참고자료

- **서울시 응급실 이용자 수**
  - 출처: [서울시 응급실 이용자 현황 – 열린데이터광장](https://data.seoul.go.kr/dataList/OA-25416/S/1/datasetView.do)
  - 설명: 서울시 자치구별 일자별 응급실 이용자 수 → 서울 전체 기준으로 집계 변환

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

