---
date: 2023-12-29
tags: Machine_Learning, 졸업작품
---

## 개념

- **두 점 간 변위로 유사도를 구함**
	- 점 사이 변위가 유사도를 결정
		- 가까울수록 유사
	- 점 P($p_1, p_2, \cdots p_n$)와 점 Q($q_1, q_2, \cdots q_n$)가 있을 때

$$Euclidean\;Distance = \sqrt{(q_1 - p_1)^2 + (q_2 - p_2)^2 + \cdots (q_n - p_n)^2} = \sqrt{\sum_{i = 1}^{n} (q_i - p_i)^2}$$

$$[1, 1, 0, 0], [0, 0, 1, 1] \rightarrow E.D = \sqrt{(1 - 0)^2 + (1 - 0)^2 + (0 - 1)^2 + (0 - 1)^2} = 2$$
$$[1, 1, 0, 0], [0, 0, 2, 2] \rightarrow E.D = \sqrt{(1 - 0)^2 + (1 - 0)^2 + (0 - 2)^2 + (0 - 2)^2} \simeq 3.162$$
