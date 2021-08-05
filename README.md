# Deep Learning

tensorflow: keras (https://www.tensorflow.org/api_docs/python/tf/keras?hl=ko)


# Step

1. 정보(데이터) 단계 
   * dropna: info(), describe()
   * fillna, replace: value_counts(), describe()
   * 컬럼 분류: 연속형, 분류형
   * 시각화
   * one-hot encoding: get_dummies
   * standard scaler 
   * data split

2. 교육 단계 
   * model make & learning
   * check score
  
3. 서비스 단계
   * pickle: model save & load
   * receive data 
   * predict


## Artificial Neural Network

* 뉴런의 작동 방식 
  * 여러 개의 시냅스로 부터 받은 여러 개의 신호(양 *시간) 를 합침. 이 값이 특정 임계점을 넘어가면 신호가 다음 시냅스로 전달됨.
  * `Activation Function` 으로 도식화 : 임계점 넘어가면 1, 아니면 0을 리턴 

* 논리 
  * AND, OR : `Single Layer Network` 
  * XOR (두 개의 input이 같지 않으면 true) : `Multi Layer Network`


## BackPropagation

* Multi Perceptron : `Input Layer,  Hidden Layer, Output Layer` 으로 구성된 머신러닝의 학습 구조. 각 층은 가중치 값으로 연결되어 있음

* BackPropagation 오차역전법 : Output layer에서 계산한 값과 내가 원하는 Target 값의 차이를 구한 후,  그 오차값 ( ex. MSE )을 뒤로 전파해가며 각 노드가 가지고 있는 변수 (가중치)를 조정하는 방법 

 ->  `Chain Rule` : 미분. 최종값 변화량에 기여하는 각 변수의 기여도를 알 수 있음

#### Step
1. 오류 계산 : 실제 출력에서 얼마나 멀리 출력되는지 계산
2. 최소 오류 : 오류가 최소화되었는지 확인
3. 매개 변수 조정 : 오류가 크면 매개 변수(가중치 및 편차)를 조정.


## Recurrent Neural Network

* 입력과 출력을 Sequence 단위로 처리하는 모델.  시간에 따라 변화하는 데이터를 학습할 때 활용  
  * `Hidden Layer`에서 `Activation Function`를 통해 나온 결과값을 `Output Layer` 에 보내거나,   
  * 다시 `Hidden Layer` 의 다음 계산의 입력으로 보내 재귀적으로 참조. (데이터 순환)
