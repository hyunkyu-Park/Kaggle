# Kaggle

21-01-26 업데이트

지난번에 의식의 흐름대로 진행을 했었는데, 방법이 잘못된 것 같아서. 전체적인 그림을 그린 후 처음부터 다시 시작했습니다.  
베이스 라인부터 시도해보려고 합니다.

1. 데이터 전처리

ㆍ 제품 변수들의 결측값을 찾아 0으로 대체합니다. 제품 보유 여부에 대한 정보가 없으면, 해당 제품을 보유하고 있지 않다고 가정합니다.  
ㆍ 예측을 위한 columns들의 대략적인 수치를 파악합니다. 만약 쓸 수 없는 column이 있다면 삭제합니다. column들을 데이터 종류(categorical, numerical, datetime)에 따라 구분합니다.  

-------------------------------------------------------------------------------------------------------------------------------  
 
21-01-27 업데이트

ㆍ 범주형(categorical), 수치형(numerical) 데이터를 전처리합니다. 범주형 데이터는 .factorize()를 통해 Label Encoding을 수행합니다. 데이터 타입이 object로 표현되는 수치형 데이터에서는 .unique()를 통해 특이 값들을 대체하거나 제거하고, 정수형 데이터로 변환해 줍니다.

2. 피처 엔지니어링

21-02-02 업데이트

ㆍ 머신러닝 모델 학습에 사용할 변수를 생성합니다. Baseline 모델에서는 고객 변수들과, 날짜 기반의 변수들, 그리고 lag-1 변수를 사용합니다.  
ㆍ 파생 변수를 사용할 때 결측값은 -99로 대체합니다.  
ㆍ lag-1 변수는 1개월 전 상품 보유 여부를 현재 고객의 데이터로 활용할 변수입니다. 추후에 lag-2, lag-3등 여러 변수를 만들어 확인할 예정입니다.  


3. 머신러닝 모델 학습

4. 테스트 데이터 예측


