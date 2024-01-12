---
date: 2023-09-19
tags: Machine_Learning
---

- [[01. Linear Regression.html]]
- [[02. Multiple Linear Regression.html]]

## 다중 선형 회귀 (Multiple Linear Regression)

- **독립 변수가 여러 개 → 다차원**
	- $y = m_1x_1 + m_2x_2 + \cdots + m_nx_n + b$
- **One-Hot Encoding**
	- 문자 데이터를 Dummy Column을 추가해서 1이나 0으로 처리
		- 표현하고 싶은 값 → 1
		- 나머지 → 0
- **다중 공선성 (Multicollinearity)**
	- <span style="border-radius: 5px; color: black; background-color: salmon">독립 변수들 간 서로 강한 상관관계</span>를 가지면서 회귀계수 추정의 오류가 나타나는 문제
		- 서로 독립이 아님
	- 해결 방법
		- Dummy Column 중 1개를 삭제 후 사용

> [출처: 파이썬 코딩 무료 강의 (활용편7) - 머신러닝, 영화 추천 시스템 만들기](https://youtu.be/TNcfJHajqJY?si=ftzrziLr5YX2hZq-)