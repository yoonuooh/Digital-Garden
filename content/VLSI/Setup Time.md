---
date: 2024-03-13
tags: VLSI
---

- [[Hold Time]]
- [[Arrival Time]]
- [[Required Time]]

## 설명

- **조건**
	- Flip-Flop 간 [[Clock Skew]]는 0이라 가정
	- Rising Edge에 Flip-Flop이 동작한다고 가정
	- Launch Flop의 Clock Edge 다음 Edge가 Capture Flop의 Clock Edge라 가정
- **Capture Flop의 Clock Edge 보다 먼저 Data가 도달해야 하는 최소 시간**

![Arrival Time](https://qph.cf2.quoracdn.net/main-qimg-a671d5e8ec3ea10496292c5d68b6537b)

![Setup Time](https://qph.cf2.quoracdn.net/main-qimg-a82305103fac294f787834ef36091ab9)



## Setup Time Violation

- **Setup Time에 데이터 변화**
	- Data가 저장되지 않음
- **해결 방법**
	- 우선 [[MTT#Maximum Transition Time Violation|MTTV]] Fix
		- 그러나 MTTV라고 Setup Time Violation은 아님