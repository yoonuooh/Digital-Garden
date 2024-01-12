---
date: 2023-09-19
tags: Machine_Learning
cssClass: purpleRed
---

- [[05. K-Means.html]]

## K-Means

- **데이터를 K개의 클러스터로 군집화하는 알고리즘**
	- 각 데이터로부터 이들이 속한 클러스터의 중심점(Centroid)까지의 평균 거리를 계산
- **동작 순서**
	- K 값 설정
	- 지정된 K개 만큼의 랜덤 좌표 설정
		- 클러스터링이 되지 않을 가능성 → <span style="color: salmon"><u>Random Initialization Trap</u></span>
	- 모든 데이터로부터 가장 가까운 중심점 선택
	- 데이터들의 평균 중심으로 중심점 이동
		- 중심점이 더 이상 이동하지 않을 때까지 반복 → 수렴
- **K-Means++**
	- Random Initialization Trap을 보완
	- 동작 순서
		- 데이터 중에서 랜덤으로 선택한 1개와 그 데이터와 가장 먼 데이터를 중심점으로 선택
		- 나머지 데이터로부터 중심점까지의 거리 계산
		- 중심점과 가장 먼 지점의 데이터를 다음 중심점으로 선택
			- 중심점이 K개가 될 때까지 반복
		- 이후 K-Means 방식과 동일
- **Elbow Method**
	- 최적의 K 구하는 방법
		- K 변화에 따른 중심점까지의 평균 거리 비교
		- 경사가 완만해지는 지점의 K를 선정 → Optimal K
- **점 간 거리**
	- [[Euclidean Distance]]
		- 변위
	- Manhattan Distance
		- 거리
	- [[Cosine Similarity]]
		- 원점과 점을 이은 선들 중 <span style="border-radius: 5px; color: black; background-color: orange">각도 차이가 적은 선끼리는 유사도가 높다고 함</span>
		- 벡터의 크기보다 각도에 중점

| Cosine Similarity Example | 문장 1 | 문장 2 | 문장 3 |
|:-------------------------:|:------:|:------:|:------:|
|          문장 1           |   1    |  0.3   |  0.8   |
|          문장 2           |  0.3   |   1    |  0.5   |
|          문장 3           |  0.8   |  0.5   | 1       |

> [출처: 파이썬 코딩 무료 강의 (활용편7) - 머신러닝, 영화 추천 시스템 만들기](https://youtu.be/TNcfJHajqJY?si=ftzrziLr5YX2hZq-)