# Statistics 200201

### 회귀분석

- 데이터의 관계성을 기술하는 것, 다시 말해 하나의 변수로 다른 변수의 값을 예측하거나 설명하는 것
- 평균값으로의 회귀 : 실제 데이터는 이론상으로 추측한 값보다 '평균값에 가까워진다'
    - 평균값으로의 회귀 현상이 일어나는 이유 : 신장, 지능 혹은 생물의 특징에만 국한되지 않고 이 세상의 모든 현상에는 다양한 '불규칙성'이 있기 때문이다.
    - ex) 올림픽 대표로 최근 대회 기록이 뛰어난 선수를 선발하지만 실제 올림픽에 나가서는 기대만큼 좋은 성적을 내지 못하는 경우가 있다. 이 역시 평균값으로의 회귀의 일례이며, 스포츠 결과가 불규칙성을 가지고 있기 때문에 생기는 현상이다.
- 불규칙성이 생기는 현상에 대해서는 이론적인 예측을 제대로 할 수 없다. 따라서 올바른 데이터를 모아 회귀분석을 할 필요가 있다.
- 회귀분석을 통해 '가장 그럴듯한 예측결과'를 얻은 것만으로 만족해서는 안 된다. 그 예측 결과는 데이터와의 오차를 최소화하는 방법으로 얻어졌다고는 해도 여전히 오차가 존재할 가능성은 남아 있다. 오차를 무시한 분석은 위험하다.

### 회귀계수 자체에 불규칙성이 있다

- 현대 통계학에서는, 실제로 얻어진 데이터 자체에 불규칙성이 존재할 뿐만 아니라, 얻어진 회귀계수 자체에도 불규칙성이 존재한다고 판단한다.
- 회귀계수에만 국한되지 않고 데이터의 평균값처럼 단순한 것일지라도, 몇 번이고 데이터를 수집해 무슨 값(통계량)이든 계산하면 매번 산출되는 통계량은 달라지게 마련이다.

### 통계학자도 이해하지 못했던 '참값'의 의미

- 피셔는 '무한히 데이터를 얻으면 마땅히 알게 되는, 진정으로 알고 싶은 값'을 참값이라 정의했다.
- 우연히 얻어진 데이터를 통해 계산한 통계량이 어느 정도의 오차로 참값을 추정할 수 있는지 수학적으로 정리함으로써 무한정 데이터를 모으지 않고도 적절한 판단이 가능하다는 생각을 피력했다.
- 현실의 데이터로부터 얻어지는 회귀계수 등의 통계량은 어디까지나 이 참값에 대한 추정치이다. 단지 가장 타당한 값을 추정하는 데서 그치는 게 아니라, 참값에 대해 어느 정도의 오차를 가지는지 판단하면 잘못된 결정을 내릴 위험성을 최소한으로 줄일 수 있다.

### 회귀분석 기초 용어

- 회귀계수의 추정치 : 절편과 기울기(x)는 모두 데이터로부터 산출된 값이지만 어디까지나 데이터에 근거해 '참값'을 추정한 결과라는 점에 주의
- 표준오차 : 추정치의 오차 크기. 회귀계수의 추정치와 비교했을 때 크게 나타나면 그다지 신뢰할 수 없지만, 이 값 자체를 문제로 삼기보다는 신뢰구간에서 생각하는 편이 낫다.
- 95% 신뢰구간 : '회귀계수가 0'의 경우뿐만 아니라 다양한 회귀계수를 상정해, 'p값이 5% 이하의 참값으로서 존재할 수 없는 값'이 되지 않는 범위. '거의 이 범위 안에 참값이 있다'고 생각해도 무방하다.
- p값 : 회귀계수가 0이었을 경우 단지 데이터의 불규칙성 때문에 이 정도의 회귀계수로 추정될 수 있는 확률. 일반적으로 5%를 웃돌면 '회귀계수 0으로 생각하기는 어렵다'라고 판단하게 된다.
- t검정 : t분포를 사용한 검정의 방식으로, 2개의 정규분포에 따르는 모집단에서 추출된 표본자료로부터 모평균이 같은가 아닌가를 검정하거나, 하나의 정규 모집단에서 추출된 표본 자료로부터 계산되는 표본평균이 모평균에 같은가 아닌가를 검정하는 등에 사용한다.