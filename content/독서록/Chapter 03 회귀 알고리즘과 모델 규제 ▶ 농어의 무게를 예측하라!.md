---
date: 2023-12-26
tags: 독서록, Machine_Learning
---

- [[Chap_03_1.html]]
- [[Chap_03_2.html]]
- [[Chap_03_3.html]]

## k-최근접 이웃 회귀

- **가장 가까운 k개 데이터의 평균**
	- 평가 기준
		- [[회귀 모델 평가|결정계수와 MAE]]



## Overfitting, Underfitting

- **Overfitting**
	- 훈련 세트 점수 » 테스트 세트 점수
		- <span style="border-radius: 5px; color: black; background-color: lightsteelblue">훈련 세트에 대해서만 과도하게 학습된 상태</span>
	- 해결 방법
		- 모델을 덜 복잡하게 함
			- k-최근접 이웃 회귀 기준 <span style="color: lightsteelblue">이웃의 개수 ↑</span>
				- 데이터 전반에 있는 일반적인 패턴 강화
- **Underfitting**
	- 훈련 세트 점수 « 테스트 세트 점수 or 두 점수 모두 낮은 경우
		- <span style="border-radius: 5px; color: black; background-color: plum">학습이 덜 된 상태</span>
	- 해결 방법
		- 모델을 더 복잡하게 함
			- k-최근접 이웃 회귀 기준 <span style="color: plum">이웃의 개수 ↓</span>
				- 데이터의 국지적인 패턴 강화



## 모델 기반 학습과 사례 기반 학습

- 모델 기반 학습
	- 모델 파라미터를 찾는 것
	- Linear Regression
- 사례 기반 학습
	- 훈련 세트를 저장하는 것이 훈련
	- k-최근접 이웃



## Linear Regression

- <span style="border-radius: 5px; color: black; background-color: thistle">단일 독립변수 n차 방정식 → 직선</span>
- 모델 파라미터
	- 기울기 (계수 or 가중치)
	- y절편
- **과대적합 규제**
	- Ridge
		- 규제 ∝ alpha
		- <span style="color: darkkhaki">계수를 제곱한 값을 기준으로 규제</span>
	- Lasso
		- 규제 ∝ alpha
		- <span style="color: lightgreen">계수의 절댓값을 기준으로 규제</span>
		- 계수를 0으로 만들 수 있음



## Polynomial Regression

- <span style="border-radius: 5px; color: black; background-color: salmon">단일 독립변수 n차 방정식 → 곡선</span>



## Multiple Regression

- <span style="border-radius: 5px; color: black; background-color: orange">복합 독립변수 1차 방정식 → 면</span>
	- 각 특성을 Linear Regression으로 학습
	- Linear Regression은 특성이 많을수록 좋음
	- 특성 공학
		- 기존의 특성을 사용해서 새로운 특성을 만드는 것
	- 특성 개수 > 샘플 개수
		- Overfitting → 규제 필요
	- 하이퍼파라미터
		- 머신러닝 모델이 학습할 수 없고 사람이 알려줘야 하는 파라미터