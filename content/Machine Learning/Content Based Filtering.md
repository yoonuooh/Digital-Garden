---
date: 2023-09-19
tags: Machine_Learning
cssClass: purpleRed
---

## Content Based Filtering

- **Bag Of Words (BOW)**
	- Feature Vectorization
	- [[TF-IDF]]
		- <span style="border-radius: 5px; color: black; background-color: salmon">자주 나오는 단어가 다른 문서에서도 자주 등장하면 중요하지 않다고 판단 → 페널티</span>
	- CountVectorizer
		- 단순 개수 세기
	- 문장 1 : I am a boy
	- 문장 2 : I am a girl
    
| Feature Vectorization |  I  | am  |  a  | boy | girl |
|:---------------------:|:---:|:---:|:---:|:---:|:----:|
|        문장 1         |  1  |  1  |  1  |  1  |  0   |
|        문장 2         |  1  |  1  |  1  |  0  |  1   |

> [출처: 파이썬 코딩 무료 강의 (활용편7) - 머신러닝, 영화 추천 시스템 만들기](https://youtu.be/TNcfJHajqJY?si=ftzrziLr5YX2hZq-)