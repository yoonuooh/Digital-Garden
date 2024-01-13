---
date: 2023-09-18
tags:
  - Data_Structure
cssclasses:
  - purpleRed
---

## Array List

```mermaid
flowchart TB
	a[0];
	b[1];
	c[2];
```

- **List 종류**
	- Array List
		- 배열 기반의 리스트
		- <span style="border-radius: 5px; color: black; background-color: salmon">메모리 공간을 연속적으로 사용</span>
	- Linked List
		- Single Linked List
		- Double LInked List
- **데이터 추가**
	- $O(1)$ or $O(N)$
		- 데이터의 크기 < Array List의 크기 → $O(1)$
		- 데이터의 크기 = Array List의 크기 → $O(N)$
			- <span style="border-radius: 5px; color: black; background-color: orange">크기가 커진 새 배열에 모든 데이터를 복사해야하기 때문</span>
- **데이터 삽입**
	- $O(N)$
	- 삽입할 인덱스 기준으로 뒤에 있는 모든 데이터를 뒤로 이동하고 삽입
- **데이터 삭제**
	- $O(N)$
	- 삭제한 데이터 인덱스 기준으로 뒤에 있는 모든 데이터를 앞으로 이동
- **데이터 검색**
	- $O(1)$
	- Random Access



## Linked List

```mermaid
flowchart LR
	a[HEAD] --> b[0] -->	c[1] --> d[2] --> e[NULL];
```

- **구조**
	- 데이터와 Next Node를 가리키는 포인터가 있는 Node로 구성
		- HEAD Node는 Dummy Node
	- 참조하지 않는 Node는 Garbage Collector가 처리
- **데이터 추가**
	- $O(N)$
	- HEAD Node부터 차례로 Node를 이동한 후 데이터 추가
- **데이터 삽입**
	- $O(N)$
	- HEAD Node부터 차례로 Node를 이동한 후 데이터 삽입
- **데이터 삭제**
	- $O(N)$
	- <span style="border-radius: 5px; color: black; background-color: khaki">삭제할 Node의 포인터를 NULL로 설정</span>
- **데이터 검색**
	- $O(N)$
	- HEAD Node부터 차례로 Node 이동



## Double Linked List

```mermaid
flowchart LR
	a[HEAD] --> b[0] -->	c[1] --> d[2] --> e[TAIL];
	e --> d --> c --> b --> a;
```

- **구조**
	- 데이터와 Next Node를 가리키는 포인터와 Prev Node를 가리키는 포인터가 있는 Node로 구성
	- HEAD Node와 TAIL Node는 Dummy Node
- **데이터 추가**
	- $O(1)$
	- TAIL Node를 통해 한 번에 데이터 추가
- **데이터 삽입**
	- $O(N)$
	- <u>HEAD나 TAIL 중 가까운 Node에서부터 검색</u>
	- Prev Node와 Curr Node 사이 포인터를 NULL로 설정
	- <span style="border-radius: 5px; color: black; background-color: lightgreen">Prev Node ↔ New Node ↔ Curr Node</span>
- **데이터 삭제**
	- $O(N)$
	- <u>HEAD나 TAIL 중 가까운 Node에서부터 검색</u>
	- Prev Node ↔ ~~Curr Node~~ ↔ Next Node
	- Curr Node의 Prev, Next 포인터를 NULL로 설정
- **데이터 검색**
	- $O(N)$
	- HEAD와 TAIL에서 동시에 검색
	- 시간 복잡도는 $O(N)$이지만 평균적으로 실제 속도는 Single Linked LIst의 절반



|  시간 복잡도  | Array List | Linked List | Double Linked List |
|:-------------:|:------------:|:-------------:|:--------------------:|
| 데이터 추가 | O(1) or O(N) |     O(N)      |         O(1)         |
| 데이터 삽입 |     O(N)     |     O(N)      |         O(N)         |
| 데이터 삭제 |     O(N)     |     O(N)      |         O(N)         |
| 데이터 검색 |     O(1)     |     O(N)      |         O(N)         |
