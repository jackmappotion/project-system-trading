# System-Trading

# 2023-11-16 Sector based analysis 부분 modulizing 에서 좀 해맴
## factor analysis 코드를 리팩토링함
## Analysis 마무리 짓고, Datasource / Analysis 에서 준비된것 기반으로 
## Model 부분 model_v1 setting


# Sector based analysis -> modulize and fancier / model part start

# Linear Coef analyser / 2d factors_analyser 작업 진행하기(둘다 prod part)

# DataSource / Analysis Production 부분 작업중 
loader / processor / fundamental analysis / technical analysis 로 나눔

# Volume Analaysis 
이평선 기반으로 거래량 평가하기:

# Fundamental Analysis 완성
# Processor 분리?
# Technical anylsis [test] 완성
- modulize 필요~

## Project repo 분리 필요
- 
analysis done
## main
데이터 엔지니어링을 진행한 부분

## backoffice
시스템 매매를 위해 [Main] 바탕으로 백오피스를 구현한것

### ETL
<img width="1024" alt="image" src="./.README_ASSETS/etl.png">

#### ETL Source
- 한국투자증권
    - ohlcv (open high low close volume etc...)
    - info (totalshares, name etc...)
- 한국전자공시시스템
    - fundamental (TotalAssets, CurrentAssets, TotalLiabilites, NetProfit etc ...)
- 한국거래소
    - KOSDAQ sector
    - KOSPI sector 

### Analysis
<img width="1024" alt="image" src="./.README_ASSETS/analysis.png">

#### Analysis Idea
- Technical Analysis
    - Linear Coefficient Related
        - Price
        - Volume
        - VolumeTurnOver
- Fundamental Analysis
    - General Factors
        - PBR, PER etc...
    - Private Factors
        - TLR (Total Liabilities Ratio), CLR (Current Liabilities Ratio) etc ...

### 
