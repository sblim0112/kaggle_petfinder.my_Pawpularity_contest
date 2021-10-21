## kaggle_petfinder.my_Pawpularity_contest
캐글 https://www.kaggle.com/c/petfinder-pawpularity-score/overview/description 

### 데이터 개요

petfinder.my는 2008년 설립된 말레이시아의 유기동물 입양 관련 플랫폼이다.

개, 고양이 뿐만아니라 조류, 햄스터 등을 포함한 약 150,000 마리 이상의 pet 데이터를 갖고 있으며, 온라인 상의 프로필과 입양률의 관계 분석 등 다양한 주제로 kaggle에서 competition을 주최하고 있다.

2019년에도 입양 예측 관련 competition을 진행하여 2,023개 팀(개인)이 참여한 바 있으며, 2021년에는 사진의 특성 데이터를 이용한 인기도 예측을 주제로 competition을 주최하여 진행중에 있다.(2021.10 ~ 2022.01) 현재 800팀(개인)이상이 참여하고 있다.

실습한 내용은 다음과 같으며, 참고한 커널은 각각의 파일에 기재하였다.


1. 시각화 EDA
* image 파일 데이터 불러오기 및 메타데이터와 image파일을 이용한 시각화 연습
* ravel() 과 flatten()의 차이 학습


2. 메타 데이터를 이용한 LGBM모델 구현 및 하이퍼 파라미터 튜닝
* 연속형 타겟변수의 분포가 bimodal 및 multimodal 경우의 데이터 분할 방법
* functools 사용하여 파생함수 연동 가능
* np.vstack, np.hstack 및 reshape를 이용한 데이터 재배열 연습
* optuna 이용, lgbm모델 하이퍼 파라미터 튜닝


3. 얻은 점
* 하이퍼 파라미터 튜닝은 중요함(타 대회 참가 시 튜닝 전후로 약 15등 정도의 순위 상승 효과를 보인 바 있음)
* 그러나 더 중요한 것은 파라미터 튜닝을 위한 실험 시 실험값의 범위 가정을 얼마나 설명 가능하게 하느냐임
* 여러 아티클과 커널을 통해 주요 모델의 파라미터 값 범위를 이론과 병행하여 학습해볼 수 있었음


### 향후 
* xgboost, catboost 등 다른 모델도 optuna 이용한 하이퍼파라미터 튜닝 구현해보기
* 딥러닝 공부 후 swin transformer까지 적용하여 rmse를 17~18 수준으로 개선
