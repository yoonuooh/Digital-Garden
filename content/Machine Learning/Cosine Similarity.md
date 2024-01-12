---
date: 2023-12-27
tags: Machine_Learning, 졸업작품
---

## 개념

- **두 벡터의 각도로 유사도를 구함**
	- 벡터의 방향이 유사도를 결정
	- 벡터의 크기는 무관

$$Cosine\;Similarity = \frac{\vec A \cdot \vec B}{\lvert A \rvert \lvert B \rvert} = \frac{\sum_{i = 1}^{n}\vec A_i \cdot \vec B_i}{\sqrt{\sum_{i = 1}^{n}{A_i}^2 \times \sum_{i = 1}^{n}{B_i}^2}}$$
$$[1, 1, 0], [0, 1, 1] \rightarrow sim = \frac{0 + 1 + 0}{\sqrt{1 + 1 + 0} \sqrt{0 + 1 + 1}} = \frac{1}{2} = 0.5$$
$$[1, 1, 0], [2, 2, 0] \rightarrow sim = \frac{2 + 2 + 0}{\sqrt{1 + 1 + 0} \sqrt{4 + 4 + 0}} = \frac{4}{\sqrt{16}} = 1$$
