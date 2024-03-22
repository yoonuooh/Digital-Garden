---
date: 2024-03-13
tags: VLSI
---

- [[Setup Time]]
- [[Arrival Time]]
- [[Required Time]]

## 설명

- **조건**
	- Flip-Flop 간 [[Clock Skew]]는 0이라 가정
	- Rising Edge에 Flip-Flop이 동작한다고 가정
	- Launch Flop의 Clock Edge 다음 Edge가 Capture Flop의 Clock Edge라 가정
- **Launch Flop의 Clock Edge와 같은 사이클인 Capture Flop의 Clock Edge 기준으로 이전 Data가 유지되어야 하는 최소 시간**


![Arrival Time](https://qph.cf2.quoracdn.net/main-qimg-a671d5e8ec3ea10496292c5d68b6537b)

![Setup Time](https://qph.cf2.quoracdn.net/main-qimg-a82305103fac294f787834ef36091ab9)



## Hold Time Violation

- **Hold Time에 input 변화**
	- 데이터가 저장되지 않음
	- 이전 데이터 유지
	- <span style="border-radius: 5px; color: black; background-color: salmon">Chip hold</span>
- **해결 방법**
	- Data input pin 앞 단에 Buffer 삽입하여 Delay 추가