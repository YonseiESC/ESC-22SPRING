# 22-1 ESC Final Project Guideline

## choose dataset

각 조에서 어떤 데이터셋을 가지고 파이널 프로젝트를 진행할지 선택합니다. 아래 소개된 데이터셋 중에서 선택해도 되고, 다른 컴피티션의 데이터셋을 사용해도 됩니다. 소개된 데이터셋이 아닌 다른 컴피티션의 데이터셋을 사용하고 싶다면 [Kaggle Competitions](https://www.kaggle.com/competitions)에 접속해서 찾아보시면 됩니다. (cv keyword: image/video/vision 등, time series keyword: time/forecast 등)

**cv dataset examples**

- [Digit Recognizer](https://www.kaggle.com/competitions/digit-recognizer-  ㅇ
- [UNIFESP X-ray Body Part Classifier](https://www.kaggle.com/competitions/unifesp-x-ray-body-part-classifier/overview)

**time series dataset examples**

- [Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/overview)
- [COVID19 Global Forecasting (Week 4)](https://www.kaggle.com/competitions/covid19-global-forecasting-week-4/overview)
- [G-Research Crypto Forecasting](https://www.kaggle.com/competitions/g-research-crypto-forecasting/overview)
- [Ubiquant Market Prediction](https://www.kaggle.com/competitions/ubiquant-market-prediction/overview)

1. 날짜별로 어떤 가게의 어떤 물품이 얼마만큼 팔렸는지를 예측하는 문제! getting started이긴 한데 추가적으로 주어지는 데이터들이 많아서 각팀이 얼마만큼 하느냐에 달린 문제일 것 같음!
https://www.kaggle.com/competitions/store-sales-time-series-forecasting/code 

2. 코로나 확진자, 사망자 예측문제! 국가랑 날짜 정보 외에는 제공되는 데이터가 없어서 힘들것같기도…(그냥 예측하긴 쉽겠지만 더 뭐 할게 없어서 발표할 내용이 없을 것 같아서 힘들것같다는 의미)
https://www.kaggle.com/competitions/covid19-global-forecasting-week-4/data 

3. 가상화폐 가격예측 문제! 여러개의 가상화폐들에 대해서 시가, 종가, 거래량으로 수익을 예측하는 문제
https://www.kaggle.com/competitions/g-research-crypto-forecasting/data?select=train.csv 

4. 이것도 비슷한 가격 에측 문제..! 근데 데이터 용량이 엄청 크다… 3번이랑 비슷해서 빼도 될 것 같기도… 
https://www.kaggle.com/competitions/ubiquant-market-prediction/data 


## week 1

## week 2

## Workflow

**1주차 : Choose dataset / Pre-processing / Feature Extraction / EDA+Visualization**

데이터 분석 이전에 데이터의 개형을 파악하고 직관을 얻는 단계입니다. 해야할 일은 다음과 같습니다. 

- **Choosing Dataset** : 아래 소개될 데이터셋 중 하나를 선택합니다. 꼭 주어진 데이터를 선택하지 않아도 됩니다. 제시된 데이터셋이 아닌 새로운 데이터를 사용하거나, 제공된 데이터의 예측 변수를 다른 변수로 정의하거나, 추가로 데이터를 붙여서 분석을 하는 것 모두 좋습니다.
  **⏰ 5월 13일 금요일 오후 7시까지 학술부장에게 개인톡으로 어떤 데이터셋을 사용할건지 알려주세요.  **

- **Pre-Processing** : 데이터의 특성상 전처리가 필요한 경우가 있습니다. 예를 들어, 시계열 변수가 포함되어 있거나, 범주형 변수를 numeric하게 코딩하기, NA imputation 등이 있을 수 있습니다. 또한 데이터의 분포와 단위 차이를 모두 고려하여 적절하게 변환 및 스케일링을 해야 합니다. 모든 변수의 분포가 같을 필요는 없지만, 같은 단위에 있는 것이 바람직합니다. 

- **Feature Extraction** : 여러 변수를 합쳐서 새로운 변수를 만들거나, 외부 데이터에서 얻은 변수로 새로운 feature를 추가하거나, correlation analysis 등을 통해 multicolinearity가 있는 변수를 분석에서 제외하는 등의 작업입니다. 변수들 끼리 상관관계가 높은 경우 단순히 삭제를 할 수도 있고, 잠재변수를 바탕으로 새로운 변수를 만들 수도 있습니다.

  📍 **주의: 변수 선택 단계가 아닙니다! 변수 선택은 모델을 세우고 난 후에 진행합니다!**

- **EDA+Visualization** : EDA는 Pre-Processing과 Feature Extraction과 병행하여 데이터에 대해 알아가는 1주차 전반에 걸쳐 시행합니다. 기본적인 기술통계량이나 skewness를 보거나, normal assumption을 적용할 수 있는지, 변수 재정의가 필요하지는 않은지 파악합니다. 또한, 데이터의 분포를 눈으로 파악하는 것이 직관을 줄 수 있습니다. 설명변수와 응답변수 간, 혹은 설명변수 간의 산점도를 그려 선형/비선형 관계를 파악하거나, 데이터 이해에 도움이 되는 시각화를 해봅니다.

📚 reference : 1주차 / 5주차 데이터 분석 예시 노트북, 공모전 리더보드, ESC 예전 파이널 프로젝트 repo 등등!

cv 팀으 이렇게 전처리가 많이 필요하지 않을텐데...


👩🏻‍💻 **중간점검 (Week 10 : May 27th)** : 다음 주 세션에서 이번학기 새로 부임하신 정성현 교수님이 30분 정도 짧게 특강을 해 주실 예정입니다! 교수님 특강 후에 조별로 돌아가면서 10분 내외로 간단하게 소개한 데이터 설명, 1주차 수행 결과를 간단히 발표해주시고, 어려운 점이나 궁금한 점을 공유해주시면 됩니다.



**2주차 : Modeling / Model Selection / Interpretation**

Bayesian Linear Regression 방법을 사용해 전 주에 준비한 설명변수들을 종합적으로 고려하여 모델을 만듭니다.

- **Modeling** : Frequentist 관점에서 일반적인 회귀 모형을 우선 적합시켜 보고, Bayesian Linear Regression을 통해서도 학습을 진행합니다. 두 방법론 간에 어떤 차이가 있을까요?

- **Model Selection** : 모델 설렉션의 의미는 크게 2 가지입니다. 모델의 CV 에러(Bias - Variance Tradeoff), 모델의 해석 가능 여부 등을 고려합니다.

  1. 모델 자체의 선택: 예컨대 로지스틱 회귀를 쓸지, SVM을 쓸지, Random Forest를 쓸지, 혹은 이 모두를 함께 쓰는 Voting Classifier를 쓸지 결정합니다.
  2. 모델 내 변수의 선택: 어떤 변수를 쓸지, 어떤 잠재변수를 고려할지 등을 결정합니다. (이번 주에 배운 내용!)

  그렇지만 이번 프로젝트의 경우 크게 linear regression 한 가지 모델을 사용하기 때문에 2번 모델 내 변수의 선택에 해당합니다.

  빈도론적 관점에서 회귀분석을 실시하였다면 forward / backward selection, information criterion 등을 사용하여 model selection을 할 수 있겠고, 이번 주에 배운 내용을 토대로 Bayesian model selection을 통해서도 feature selection을 하여 결과를 비교해보세요. 두 관점 모두에서 적용 및 해석이 가능한 Lasso / Ridge 등의 penalizing method를 사용할 수도 있습니다.

- **Interpretation** : Evaluation이 주된 목적은 아니지만 분석 과제에 맞게 metric을 정하고 그를 바탕으로 모델의 성능을 평가합니다. 공모전 데이터처럼 metric이나 평가에 사용하는 score가 정해져 있는 경우도 있고, 단순 MSE를 사용할 수도, binary classification이라면 contingency table을 보는 방법 등이 있습니다. 잘 예측하는 것도 중요하지만 그에 못지않게 모델을 설명할 수 있는 것도 중요합니다. 예를 들어, 어떤 변수가 중요한지 (나아가 왜 중요한지 나름의 해석이 있으면 좋겠죠?), 회귀 계수나 feature selection의 Importance 값을 근거로 제시하고 그 이유를 생각해보면 됩니다.

  

👩🏻‍💻 **최종 발표 (Week 11 : June 3rd)** : 2주 간 파이널 프로젝트를 수행한 내용을 팀별로 15분 이내로 발표해주세요. 뉴럴넷이나 부스팅 등의 방법을 사용하지 않기 때문에 score 자체는 좋지 않을 수도 있습니다. 이번 프로젝트에서는 결과가 좋지 않더라도 왜 좋지 않았을지 생각해본 내용이나 improvement 등을 고민해보시고 발표해주세요. 한 학기동안 배운 내용과 연관지어 결과를 잘 해석하고 모델과 변수를 잘 설명하는 게 중요합니다!

## datasets

data 소개 - goal - link - 특이사항 및 조언(?)

cv
https://www.kaggle.com/competitions/digit-recognizer/leaderboard
https://www.kaggle.com/competitions/unifesp-x-ray-body-part-classifier/data


time series
https://www.kaggle.com/competitions/store-sales-time-series-forecasting/code
https://www.kaggle.com/competitions/ubiquant-market-prediction/data



## Reference

towards data science articles
