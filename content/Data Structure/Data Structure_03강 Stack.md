---
date: 2023-09-22
tags: Data_Structure
---

## Stack

```mermaid
flowchart TB
	a[HEAD] --> b[0] --> c[1] --> d[2] --> e[NULL]
```

- **Linked List와 유사**
	- HEAD → NULL
- **LIFO**
	- Last-In-First-Out
	- 후입선출
- **연산**
	- push()
		- 데이터 추가
	- pop()
		- 데이터 삭제
	- top(), peek()
		- 가장 앞 데이터 검색