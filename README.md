# Project-Name and Description
- Project Name : Trading system using two kinds of Autoencoder

  (Conditional Auto Encoder와 Original Autoencoder 을 이용한 주식 매매 전략 프로젝트).
  
- Description : AI competition hosted by the Ulsan National Institute of Science and Technology(UNIST).

# Project Period
- 2023.04 ~ 2023.11

# Introcdution of team
- Two business analytics students of  master course

- One computer science bachelor student

# Project Result
- The Visitors' choice Award(78 votes, Second Ranker)

*First Ranker(98 votes), Third Ranker(54 votes)*

# The paper
- Autoencoder asset pricing models(Journal of Econometrics)

- 딥러닝을 활용한 자산분배 시스템(Journal of the Korea Industrial Information Systems Research)

- 딥 러닝을 이용한 포트폴리오 구성 전략(Journal of Information Technology and Architecture)

# How the project is run
-

# Limition of the project
- 일 거래량이 적은 종목은 매수를 할 수가 없다. 왜냐하면 sharpe ratio기반 10000개의 포트폴리오 비중의 경우의 수로 종목별 매수 비중을 고려하는데 간혹 거래량이 거의 없는 주식의 일 거래량을 넘어서는 수량 혹은 거의 근사치에 가까운 수량을 추천할 경우 한 개인이 해당 주식을 거래량을 모두 구매할 수 없다. 따라서 거래량이 많은 대형주 위주로 주식 종목을 추천하는 한계점을 가지고 있다.

- Original Autoencoder를보면 validation loss가 train loss보다 loss 값이 더 적은 그림을 볼 수 있다. 이 문제를 해결하기 위해서 정말 많이 코드를 수정해보고 학습률, 최적화도 바꿔보았지만 쉽지 않았다. 하지만 케라스 공식문서에 오토인코더를 사용할 때 우리와 같은 사례가 종종 발견되어 해당 내용을 정리한 문서를 발견하였다.

*훈련 손실이 테스트 손실보다 훨씬 높은 이유는 무엇입니까?
Keras 모델에는 훈련과 테스트라는 두 가지 모드가 있습니다. Dropout 및 L1/L2 가중치 정규화와 같은 정규화 메커니즘은 테스트 시 꺼집니다. 훈련 시간 손실에는 반영되지만 테스트 시간 손실에는 반영되지 않습니다.
게다가 Keras가 표시하는 훈련 손실은 현재 epoch 동안 각 훈련 데이터 배치에 대한 손실의 평균입니다 . 모델은 시간이 지남에 따라 변경되므로 한 에포크의 첫 번째 배치에 대한 손실은 일반적으로 마지막 배치에 대한 손실보다 높습니다. 이로 인해 에포크별 평균이 낮아질 수 있습니다. 반면, 한 에포크에 대한 테스트 손실은 에포크가 끝날 때의 모델을 그대로 사용하여 계산되므로 손실이 더 낮습니다.* (https://keras.io/getting_started/faq/#why-is-my-training-loss-much-higher-than-my-testing-loss)

- Original Autoencoder와 Conditional Autoencoder의 포트폴리오 수익률과 순위를 비교하는데 등락이 보이는 구간이 있다. 등락이 왔다갔다하는 이유로 떠오르는 합리적인 이유로는 앞서 우리가 Sharpe ratio를 통해서 10000개의 포트폴리오를 만드는데, 10000개를 만드는 과정이 랜덤 확률에 맞추어 만들어지므로 등락이 왔다갔다하는 경향이 보인다고 생각한다.


# Keyword
- Original Autoencoder
- Conditional Autoencoder
- Sharpe Ratio
- Deep Learning
