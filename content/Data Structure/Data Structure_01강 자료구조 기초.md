---
date: 2023-09-18
tags: Data_Structure
---

## 자료 구조란

- **자료 구조란**
	- 자료를 담는 추상적인 틀
- **가장 적합한 자료 구조를 쓰는 것이 중요**
	- 컴퓨터의 자원이 한정적이기 때문
	- 제한된 제약조건 내에 정확한 결과를 내야하기 때문
	- 자료 구조 하나를 잘못 쓰면 시스템 전체가 매우 느려질 수 있기 떄문
- **알고리즘**
	- 어떤 문제가 주어졌을 때 문제를 풀기 위한 동작들의 절차



## Big-O 표기법

- **Big-O 표기법**
	- 점근 표기법[^1] 특징
		- 가장 큰 영향력이 있는 항만 취급
		- 상수항 무시
	- 공간 복잡도
		- <span style="color: salmon">데이터 관리에 필요한 공간</span>
		- 데이터 양의 변화에 따른 공간의 변화
		- 예상 소요 공간 측정
	- 시간 복잡도
		- <span style="color: orange">데이터 처리에 소요되는 시간</span>
		- 데이터 양의 변화에 따른 소요 시간의 변화
		- 예상 처리 시간 측정



## 시간 복잡도

- $O(1)$
	- 입력 데이터의 <span style="color: darkkhaki">크기와 상관없이 항상 일정한 시간</span>이 걸리는 알고리즘
	- 배열의 Random Access
	- Hash
- $O(N)$
	- 입력 데이터의 <span style="color: lightgreen">크기에 비례해서 시간</span>이 소요되는 알고리즘
	- for문
- $O(N^2)$
	- 입력 데이터의 <span style="color: lightblue">제곱에 비례해서 시간</span>이 소요되는 알고리즘
	- 이중 for문
- $O(log_2N)$
	- <span style="color: lightsteelblue">이진탐색</span>
		- 숫자 범위를 절반씩 좁혀가는 탐색 방법
- $O(Nlog_2N)$
	- <span style="color: plum">Merge sort</span>
		- 한 묶음이 2개가 될 때까지 절반씩 나눈 다음 정렬

[^1]: Big-O 표기법, 세타 표기법, 오메가 표기법