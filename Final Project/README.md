# 22-1 ESC Final Project Guideline

## choose dataset

각 조에서 어떤 데이터셋을 가지고 파이널 프로젝트를 진행할지 선택합니다. 아래 소개된 데이터셋 중에서 선택해도 되고, 다른 컴피티션의 데이터셋을 사용해도 됩니다. 소개된 데이터셋이 아닌 다른 컴피티션의 데이터셋을 사용하고 싶다면 [Kaggle Competitions](https://www.kaggle.com/competitions)에 접속해서 찾아보시면 됩니다. 

  **⏰ 5월 13일 금요일까지 어떤 데이터셋을 사용할 것인지 선택해주시기 바랍니다!**

🗂 **cv dataset examples**

1. [**Digit Recognizer**](https://www.kaggle.com/competitions/digit-recognizer)
- 지금까지 많이 접했었던 MNIST 데이터셋입니다! 손글씨 이미지 데이터를 통해 그것이 무슨 숫자인지 예측하는 데이터셋
- 이런 경우에 단순히 모델 하나를 적용하기 보다는 다양한 모델을 적용해서 비교해보기도 하고, 데이터 전처리를 통해 데이터의 수를 늘려보기도 하고, 하이퍼파라미터 튜닝을 통해 최적의 모델을 찾는 등 성능을 최고로 끌어내는 것을 목표로 삼아볼 수 잇겠죠! 

2. [**UNIFESP X-ray Body Part Classifier**](https://www.kaggle.com/competitions/unifesp-x-ray-body-part-classifier/overview)
- 이미지 분류 문제입니다! 각 엑스레이 이미지를 가지고 그 사진이 신체의 어느 부분을 찍은 것인지를 예측하는 문제
- MNIST와 비슷하게 성능을 끌어올리는 것이 목표

이 외에도 [Kaggle Competitions](https://www.kaggle.com/competitions)에서 image/video/vision 등을 검색해보시면 다양한 CV 컴피티션을 찾을 수 있습니다. 

🗂 **time series dataset examples**

1. [**Store Sales - Time Series Forecasting**](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/overview)
- 날짜별로 어떤 가게의 어떤 물품이 얼마만큼 팔렸는지를 에측하는 문제, 
- 기본 컴피티션이긴 하지만, train데이터셋 외에도 다양한 정보가 제공되기 때문에 이 정보들을 어떻게 활용할지가 관건인 컴피티션입니다! 


2. [**COVID19 Global Forecasting (Week 4)**](https://www.kaggle.com/competitions/covid19-global-forecasting-week-4/overview)
- 세계 각국의 코로나 확진자, 사망자 추이 예측 문제입니다. 4주차만 걸어놨지만 1주차부터 5주차까지의 데이터를 확인하실 수 있습니다. 
- 다만 국가와 날짜 정보 외에는 feature 로 사용할만한 데이터가 없어서 파이널 프로젝트로 진행하기에는 조금 어려울 수 있을 것 같습니다. 
- 다만 외부 데이터를 찾아서 활용하거나, 다양한 시계열 예측 모델들을 적용해서 비교해보거나, 성능을 최대한 향상시키는 방향으로 진행해볼 수 있습니다 

3. [**G-Research Crypto Forecasting**](https://www.kaggle.com/competitions/g-research-crypto-forecasting/overview)
- 여러가지 가상화폐의 시가, 종가, 거래량 등의 정보를 통해 수익을 예측하는 문제입니다! 

4. [**Ubiquant Market Prediction**](https://www.kaggle.com/competitions/ubiquant-market-prediction/overview)
- 3번과 비슷한 가격 에측문제입니다! 
- 이런 데이터셋의 경우 용량이 엄청 크기 때문에 이점 유의하셔서 선택해주셔야 합니다. 

이 외에도 [Kaggle Competitions](https://www.kaggle.com/competitions)에서 time/forecast 등을 검색해보시면 다양한 시계열 예측 컴피티션을 찾을 수 있습니다. 

## week 1

1주차에 해야할 일은 다음과 같습니다. 모든 단계를 해야하는 것은 아니고 각 조의 프로젝트 상황에 맞게 수행해주시면 됩니다. 

**pre-processing / feature extraction / EDA + Visualization / baseline model**

- **Pre-Processing** : 데이터의 특성상 전처리가 필요한 경우가 있습니다. 예를 들어, 시계열 변수가 포함되어 있거나, 범주형 변수를 numeric하게 코딩하기, NA imputation 등이 있을 수 있습니다. 또한 데이터의 분포와 단위 차이를 모두 고려하여 적절하게 변환 및 스케일링을 해야 합니다. 모든 변수의 분포가 같을 필요는 없지만, 같은 단위에 있는 것이 바람직합니다. 

- **Feature Extraction** : 여러 변수를 합쳐서 새로운 변수를 만들거나, 외부 데이터에서 얻은 변수로 새로운 feature를 추가하거나, correlation analysis 등을 통해 multicolinearity가 있는 변수를 분석에서 제외하는 등의 작업입니다. 변수들 끼리 상관관계가 높은 경우 단순히 삭제를 할 수도 있고, 잠재변수를 바탕으로 새로운 변수를 만들 수도 있습니다.

  📍 **주의: 변수 선택 단계가 아닙니다! 변수 선택은 모델을 세우고 난 후에 진행합니다!**

- **EDA+Visualization** : EDA는 Pre-Processing과 Feature Extraction과 병행하여 데이터에 대해 알아가는 1주차 전반에 걸쳐 시행합니다. 기본적인 기술통계량이나 skewness를 보거나, normal assumption을 적용할 수 있는지, 변수 재정의가 필요하지는 않은지 파악합니다. 또한, 데이터의 분포를 눈으로 파악하는 것이 직관을 줄 수 있습니다. 설명변수와 응답변수 간, 혹은 설명변수 간의 산점도를 그려 선형/비선형 관계를 파악하거나, 데이터 이해에 도움이 되는 시각화를 해봅니다. 

- **Baseline model** : 성능향상을 목표로 하는 컴피티션의 경우에, 1주차에 기본적인 모델로 피팅을 시켜 스코어 기준점을 잡아주시는 과정을 거쳐도 좋습니다. 이때의 모델은 가장 기본이 되는 바닐라 모델 쉬운 모델 등을 사용해주셔도 됩니다. 

👩‍🏫 **중간점검(5/19 목)** 조별로 돌아가면서 10분 내외로 간단하게 현재까지 진행상황 발표해주시면 됩니다. 프로젝트의 목표, 데이터 개형, 1주차 수행 결과 및 앞으로의 계획, 진행하면서 어려운 점이나 궁금한 점 등을 공유해주시면 됩니다. 

## week 2


**Modeling / Model Selection / Evaluation**

Bayesian Linear Regression 방법을 사용해 전 주에 준비한 설명변수들을 종합적으로 고려하여 모델을 만듭니다.

- **Modeling** : Frequentist 관점에서 일반적인 회귀 모형을 우선 적합시켜 보고, Bayesian Linear Regression을 통해서도 학습을 진행합니다. 두 방법론 간에 어떤 차이가 있을까요?

- **Model Selection** : 모델 설렉션의 의미는 크게 2 가지입니다. 모델의 CV 에러(Bias - Variance Tradeoff), 모델의 해석 가능 여부 등을 고려합니다.

  1. 모델 자체의 선택: 예컨대 로지스틱 회귀를 쓸지, SVM을 쓸지, Random Forest를 쓸지, 혹은 이 모두를 함께 쓰는 Voting Classifier를 쓸지 결정합니다.
  2. 모델 내 변수의 선택: 어떤 변수를 쓸지, 어떤 잠재변수를 고려할지 등을 결정합니다. (이번 주에 배운 내용!)

  그렇지만 이번 프로젝트의 경우 크게 linear regression 한 가지 모델을 사용하기 때문에 2번 모델 내 변수의 선택에 해당합니다.

  빈도론적 관점에서 회귀분석을 실시하였다면 forward / backward selection, information criterion 등을 사용하여 model selection을 할 수 있겠고, 이번 주에 배운 내용을 토대로 Bayesian model selection을 통해서도 feature selection을 하여 결과를 비교해보세요. 두 관점 모두에서 적용 및 해석이 가능한 Lasso / Ridge 등의 penalizing method를 사용할 수도 있습니다.

- **Evaluation** : 분석 과제에 맞게 metric을 정하고 그를 바탕으로 모델의 성능을 평가합니다. 캐글 컴피티션의 경우 overview > evaluation 에 들어가면 어떤 score를 사용하는지를 확인하실 수 있습니다.

👩‍🏫 **최종발표(5/27 목)** 2주간 파이널 프로젝트를 수행한 내용을 팀별로 15분 이내로 발표해주세요. 어떤 모델을 사용했는지, 왜 그 모델을 선택했는지, 다른 모델과 비교해보았을 때  score가 어떻게 개선되었는지 등을 공유해주시면 됩니다. 진행하면서 어려웠던 점이나 아쉬웠던 점, 궁금했던 점들 공유해주셔도 됩니다. 

## Reference

각 컴피티션 리더보드

이전기수 파이널프로젝트 repository

https://towardsdatascience.com/baseline-models-your-guide-for-model-building-1ec3aa244b8d

towards data science articles
