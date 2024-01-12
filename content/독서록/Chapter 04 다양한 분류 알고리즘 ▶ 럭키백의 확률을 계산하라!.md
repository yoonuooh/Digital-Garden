---
date: 2023-12-26
tags: 독서록, Machine_Learning
---

- [[Chap_04_1.html]]

- **Logistic Regression**
	- 선형 방정식을 계산 후 값을 0 ~ 1 사이로 출력
	- 이진 분류
		- <span style="color: lightblue">SIgmoid Function</span>
			- 하나의 선형 방정식의 출력값을 0 ~ 1 사이로 압축
			- z = -∞ → ϕ = 0
			- z = 0 → ϕ = 0.5
			- z = ∞ → ϕ = 1
		- 규제
			- L2
				- 규제 ∝ $\frac{1}{C}$
		- $$\phi = \frac{1}{1 + e^{-z}}$$
	- 다중 분류
		- <span style="color: lightsteelblue">Softmax Function</span>
			- 클래스별로 z 값 계산
			- 여러 개의 선형 방정식의 출력값을 0 ~ 1 사이로 압축하고 <u>전체 합이 1이 되도록 정규화</u>
- **확률적 경사 하강법**