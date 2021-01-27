**EDA - Exploratory Data Analysis : 데이터 전처리** 

데이터프레임 열과 행 내부의 데이터 편집, 결측치 대체 등

**Feature Engineering  : feature들을 재조합하여 새로운 feature를 만드는 과정**

데이터프레임의 열과 행의 연산을 위해 데이터 타입을 통일하는 과정이 필요


**Data Manipulation : 데이터 조합** 

- concat : 단순히 두 개의 데이터프레임을 열이나 행 방향으로 이어 붙이는 것
- merge : 두 개의 데이터프레임에서 공통된 부분을 찾아 그 부분을 중심으로 데이터를 이어붙이는 것 → sql의 join과 비슷
- conditioning : 데이터 조합 시에 원하는 부분만 뽑아 이어 붙일 수 있도록 조건을 지정하는 과정 - 필터링 → isin, groupby 등을 이용
- tidy한 데이터를 위해 melt 함수를 이용 → melt와 반대 역할 - pivot_table


**Data Visualization : 데이터 시각화**

- matplotlib, seaborn 등의 라이브러리를 이용
- 색상을 필요에 맞게 적절히 사용하는 것은 좋은 인사이트를 얻기 위해 중요한 점


**Hypothesis Test : 가설 검정**

- 기술통계치 : count, mean, median, standard dev 등 데이터의 속성을 설명하는 값 - 주어진 표본을 요약하고 설명하는데 중점
- 추리통계치 : 수집한 데이터를 바탕으로 추론, 예측하는 통계 기법 - 표본의 자료를 토대로 가설을 검증하거나 앞으로의 현상을 예측하는 데 중점
- Sampling : 모집단에서 통계 기법을 적용하기 위한 표본을 추출하는 과정
- 가설 검정 : 설정한 가설이 옳은지 틀렸는지를 검증하는 과정 - 통계적으로 유의미한지 아닌지
- T-test : 두 집단 간 평균의 차이가 유의미한지 검증하는 통계 기법 → one sample t-test, two sample t-test
- P-value : 유의 확률, 귀무가설이 맞다는 전제 하에, 표본에서 실제로 관측된 통계치와 같거나 더 극단적인 통계치가 관측될 확률. 0~1사이의 수치이며 값이 작을수록 귀무가설을 기각한다

**Chi-square Test : 카이제곱 검정**

- one sample x^2 test : 주어진 데이터가 특정 예상되는 분포와 동일한 분포를 나타내는지에 대한 가설검정
- 카이제곱 값 : χ2 = Σ (관측값 - 기댓값)2 / 기댓값
- 동질성 검증: '변인의 분포가 이항분포나 정규분포와 동일하다'라는 가설을 설정한다. 이는 어떤 모집단의 표본이 그 모집단을 대표하고 있는지를 검증하는 데 사용한다.
- 독립성 검증: 변인이 두 개 이상일 때 사용되며, 기대빈도는 '두 변인이 서로 상관이 없고 독립적'이라고 기대하는 것을 의미하며 관찰빈도와의 차이를 통해 기대빈도의 진위여부를 밝힌다.



**Confidence Intervals : 신뢰구간**

- 큰 수의 법칙 ( Law of large numbers ) : sample 데이터의 수가 커질 수록, sample의 통계치는 점점 모집단의 모수와 같아진다.
- 중심극한정리 ( Central Limit Theorem, CLT ) : Sample 데이터의 수가 많아질 수록, sample의 평균은 정규분포에 근사한 형태로 나타난다.
- 표준 오차 : 표본 평균의 분포에 대한 표준 편차
- 신뢰도 : 신뢰구간 안에 모집단의 평균이 포함될 확률 - 모집단의 평균이 신뢰구간 안에 들어가는 경우, 귀무가설을 기각하지 않는다.


**Bayesian : 베이즈 확률론**

- 베이즈 확률론 : 지식 또는 믿음의 정도를 나타내는 양으로 확률을 해석하는 확률론 - 사후 확률이 업데이트됨에 따라 확률이 달라짐



**Vectors and Matrics : 벡터와 행렬**

벡터의 크기 : 모든 원소의 제곱을 더한 다음 루트를 씌운 값, ||v||

벡터의 내적 : 각 구성요소를 곱한 뒤 합한 값, dot product

매트릭스의 전치 : 행과 열을 바꾸는 것

정사각 매트릭스 = 정방 매트릭스 : 행과 열의 수가 동일한 매트릭스

행렬식 : det(A), 행렬식이 0인 경우 매트릭스의 행과 열이 선형 의존관계에 있음

**Linear Algebra : 선형대수**

- 분산 : 데이터가 퍼져있는 정도, 평균의 차이의 제곱 평균
- 표준편차 : 분산에 루트를 씌운 값
- 공분산 : 1개의 변수가 변화할 때 다른 변수가 어떠한 연관성을 나타내며 변하는지 측정하는 것, 값이 클수록 연관성이 높다
- 상관계수(Correlation coefficient) : 공분산을 두 변수의 표준편차로 나눠줌 - 공분산의 스케일을 조정하기 위함
- Spearman correlation coefficient : 값들에 대해서 순서 혹은 rank를 매기고, 그를 바탕으로 correlation을 측정하는 Non-parametric한 방식
- Orthogonality : 벡터나 매트릭스가 서로 수직으로 있는 상태 - 두 벡터의 내적값이 0일 때
- Span : 주어진 두 벡터의 (합이나 차와 같은) 조합으로 만들 수 있는 모든 가능한 벡터의 집합
- Basis : 벡터 공간 V의 basis 는, V라는 공간을 채울 수 있는 선형 관계에 있지 않은 벡터들의 모음( span 의 역개념 )
- Rank : span 공간의 차원
- Linear projection : 선형 투영, 데이터의 공간을 축소하기 위해 사용



**Dimensionality Reduction Techniques : 차원 축소**

Vector Transformation : 벡터 변환 - linear projection도 일종의 벡터 변환

Eigenvectors : 고유벡터, 변환에 영향을 받지 않는 회전축, 변환이 일어난 이후에도 방향이 변하지 않는 영벡터가 아닌 벡터

Eigenvalue : 고유값, 고유벡터에 대응하는 고유의 스칼라값

PCA(Principal Component Analysis) : 주성분 분석, 고차원의 데이터를 저차원의 데이터로 바꾸는 기법


**Clustering : 클러스터링**

clustering : 주어진 데이터들이 얼마나, 어떻게 유사한지에 따라 그룹을 짓는 것. 다양한 알고리즘이 존재한다.

k-means clustering : k개의 랜덤한 데이터를 cluster의 중심점으로 설정하고, 해당 cluster에 근접해 있는 데이터를 cluster로 할당한다. 그 후 변경된 cluster에 대해서 중심점을 새로 계산
