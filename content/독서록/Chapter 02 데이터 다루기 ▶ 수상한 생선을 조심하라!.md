---
date: 2023-12-26
tags: 독서록, Machine_Learning
---

- [[Chap_02_1.html]]
- [[Chap_02_2.html]]

## 지도 학습

- **데이터와 정답이 필요**



## 훈련 세트, 테스트 세트 분리

- **훈련 세트와 테스트 세트에 샘플이 골고루 섞이지 않으면 정확하지 않음**
	- <span style="border-radius: 5px; color: black; background-color: orange">샘플링 편향</span>
	- `train_input, test_input, train_target, test_target = train_test_split(fish_data, fish_target, stratify=fish_target, random_state = 42)`
		- <span style="border-radius: 5px; color: black; background-color: khaki">stratify 매개변수의 클래스 비율에 맞게 데이터 분할</span>



## 데이터 전처리

- **스케일 정규화**
	- 스케일이 다르면 거리 기반 알고리즘일 때 특히 정확하지 않음
		- 스케일을 맞춰줘야 함 → 데이터 전처리
		- 훈련 세트를 변환한 방식 그대로 테스트 세트를 변환해야 함
			- <span style="border-radius: 5px; color: black; background-color: lightgreen">반드시 훈련 세트의 평균과 표준편차로 테스트 세트 표준점수 처리</span>
	- <span style="border-radius: 5px; color: black; background-color: lightblue">표준점수</span>(z 점수)를 많이 사용
		- x : 원래 수치
		- μ : 모집단의 평균
		- σ : 모집단의 표준편차

$$z = \frac{x - \mu}{\sigma}$$