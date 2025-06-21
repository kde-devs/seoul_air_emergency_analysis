# Seoul PM2.5 and Emergency Room Visit Time-Series Analysis (2020-2021)
서울시 미세먼지와 응급실 방문 수 시계열 분석 (2020~2021)

# Overview | 개요
This project explores the time-series correlation between PM2.5 levels and emergency room visits in Seoul from 2020 to 2021
서울시의 미세먼지(PM2.5) 농도와 응급실 방문 수 사이의 시계열적 상관관게를 분석한 프로젝트입니다.

⚠️ This project was originally assigned as a team project. However, due to limited team participation, all data collection, processing, analysis, visualization, and documentation were independently completed by myself.

# Data Source | 데이터 출처
- **서울시 초미세먼지(PM2.5) 월별 농도**
  - 출처: [서울시 대기환경정보 월별 통계](https://cleanair.seoul.go.kr/statistics/monthAverage)
  - 설명: 서울시 자치구별 월별 평균 PM2.5 농도 (2020–2021)

- **서울시 응급실 이용자 수 (일별/자치구별)**
  - 출처: [서울열린데이터광장 – 응급실 이용자 현황](https://data.seoul.go.kr/dataList/11035/S/2/datasetView.do)
  - 설명: 자치구별 일자별 응급실 이용자 수 → 서울시 전체 기준으로 합산 예정
    
# Methods | 분석 방법
- Time-series alignment & smoothing
- Lag correlation analysis
- Seasonal trend decomposition

# Key Findings | 주요 결과
- A strong correlation was observed with a 1-day lag between PM2.5 peaks and emergency visits.
- Seasonal patterns showed higher ER visits during winter with elevated dust levels

# Tech Stack | 기술 스택
- Python, Pandas, Matplotlib, Seaborn, Statsmodels

# Preprocessing | 전처리 파일

## PM2.5 일별 평균값 전처리

- [전처리 노트북](https://github.com/kde-devs/seoul_air_emergency_analysis/blob/main/pm25_daily_seoul_2020_2021.ipynb)  
- [전처리 결과 CSV](https://github.com/kde-devs/seoul_air_emergency_analysis/blob/main/pm25_daily_avg_seoul_2020_2021.csv)

## 응급실 일별 이용자 수 전처리

- [전처리 노트북](https://github.com/kde-devs/seoul_air_emergency_analysis/blob/main/er_daily_seoul_2020_2021.ipynb)  
- [전처리 결과 CSV](https://github.com/kde-devs/seoul_air_emergency_analysis/blob/main/er_daily_seoul_2020_2021.csv)

> 모든 전처리 코드는 수작업으로 작성되었으며, 반복 구조 특성상 자동 생성 코드로 오인될 수 있으나 실제 데이터 분석 목적에 따라 설계된 사용자 정의 코드입니다.

> ⚠️ 분석에 사용된 PM2.5 및 응급실 이용자 수 병합 데이터는 별도 파일로 업로드하지 않았습니다.  
> 아래 두 전처리 결과 파일을 `date` 컬럼 기준으로 병합하여 재생성할 수 있습니다:
>
> - `pm25_daily_avg_seoul_2020_2021.csv`  
> - `er_daily_seoul_2020_2021.csv`
>
> 예시 코드:
>
> ```python
> merged_df = pd.merge(pm25_df, er_df, on="date", how="inner")
> ```

## Visualizations | 시각화 결과
- **[시각화 노트북 보기](https://github.com/kde-devs/seoul_air_emergency_analysis/blob/main/visualize_pm25_er_seoul.ipynb)**
- PM2.5 농도 및 응급실 방문 수 추이 (2020–2021)  
- 월별 계절성 패턴 시각화  
- 이상치 탐지 및 급증 구간 분석
⚠️ 본 시각화 노트북 역시 수작업으로 작성되었으며, 반복 구조 특성상 자동 생성된 코드처럼 보일 수 있으나, 실제 분석 목적에 따라 직접 설계된 사용자 정의 코드입니다.

## Analysis Results | 분석 결과
- 시차 상관 분석 결과 및 요약표
- STL 기반 시계열 분해 시각화
- 주요 결과 요약 및 해석

## Insights & Discussion | 시사점 및 논의
- 계절성 기반 응급실 수요 예측 가능성
- 고농도 미세먼지 대비 응급 대응 정책 제언




