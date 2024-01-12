---
date: 2023-09-19
tags: Machine_Learning
cssClass: purpleRed
---

- [[04. Logistic Regression.html]]

## Logistic Regression

- **Classfication에 해당**
	- 선형 회귀 방식을 분류에 적용한 알고리즘
	- <span style="border-radius: 5px; color: black; background-color: salmon">데이터가 어떤 범주에 속할 확률을 0과 1 사이 값으로 예측</span>
- **Sigmoid 함수**

$$y = mx + b \quad\quad P = \frac{1}{1 + e^{-y}}$$
$$ln\Big(\frac{P}{1 - P}\Big) = mx + b$$
- **Confusion Matrix**

| Confusion Matrix | 불합격 (예측) | 합격 (예측) |
|:----------------:|:-------------:|:-----------:|
|  불합격 (실제)   |       1 (True Negative)      |      1 (False Positive)     |
|   합격 (실제)    |       0 (False Negative)      |      2 (True Positive)     |

> [출처: 파이썬 코딩 무료 강의 (활용편7) - 머신러닝, 영화 추천 시스템 만들기](https://youtu.be/TNcfJHajqJY?si=ftzrziLr5YX2hZq-)