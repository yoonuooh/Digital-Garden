---
date: 2024-03-11
tags: VLSI
---

- [[Setup Time]]
- [[Hold Time]]
- [[Arrival Time]]
- [[Required Time]]
- [[Threshold]]
- [[Transition Time]]
- [[Clock Skew]]

## 설명

- **모든 Path의 Timing을 체크해서 설계의 Timing Performance가 정확한지 확인**
	- 장점
		- Runtime이 긴 시뮬레이션을 대체하기 위해서 Pre-STA 사용
			- Multiple Test Vector를 시뮬레이션할 필요가 없기 때문
		- 시뮬레이션보다 철저함
			- 가능한 경우 중 최악의 경우의 Timing을 검증하기 때문
	- 단점
		- 동기식 회로에만 효과가 있음 → [[Latch와 Flip-Flop 차이점]]
	- [[ATPG Simulation]]
- **Timing Path**
	- Data Path
		- Startpoint
			- Input port
			- Register clock pin
		- Endpoint
			- Data input pin
			- Output port
	- Clock Path
		- Startpoint
			- Clock input port
		- Endpoint
			- Clock pin
	- Clock Gating Path
		- Startpoint
			- Input port
		- Endpoint
			- Clock gating element input port
	- Asynchronous Path
		- Startpoint
			- Input port
		- Endpoint
			- Set/Reset/Clear pin
- **Library마다 Rise, Fall일 때 Maximum Delay, Minimum Delay 계산**
	- Maximum Delay
		- 가장 긴 Path Delay 계산
	- Minimum Delay
		- 가장 짧은 Path Delay 계산
	- [[Cell Delay]]
	- [[Net Delay]]

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgU1icIHqog0FgtZ6lMoq_BUOC53xQjb8H9JABsoXLDzXWd3ztmRLgQfXVrpBm5n-VLjT8bFgXsIqARvV0bci1gyrG6jRJSYF2L6tB5n5n5p8GO5vkuG38KkmhsmnlBvP53Yz0cBAbxebg/s1600/timing-path1.bmp)

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgp79lKmeILe6QMnVxv8nT_KNC5b0-bk-DY7F19Jglu_SkYf-4MvpY3V1C43SS0MVSDkP67PP-P1_lx9LEK3TBKPAkJKFhNapySKjtKYiPDJfDlCgfxoOXBnwldsq2P4_Qt0yWKqHkqWqQ/s1600/clock-path.bmp)

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhojwb9vxEDZAMU-jIiYi8Gy_egjckb0kpEggKpxxgY4D9pRUSz3YcF3js3ebv_9bkdrAyruunGkxbym4mcCr8VpzsOElsAX3Yn0xyAbYCCu4QwLDJyo-Uk26SU35p2f_u9Y1aDAZ9gEYs/s1600/clock-gating+path.bmp)

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh6W1nDVyRODG5nH7LTSfFv-mJiG7ijOEkOG_5Od_2-8gLD6BUAjLQMlMpL9FC9CRk0DNqDTgbnFxRgT4SbU0XLKYT3KyAEvoNKpVQ88uzD1g7oExq5fa8z9DWRE-SbwuWzhQMYi-vD8Dg/s1600/Asynchronous-path.bmp)



## Input / Output

- **Input**
	- Netlist
	- .db
	- SDF
	- [[SDC]]
- **Output**
	- Timing Report
	- SDF
	- SDC



## 순서

- **설계를 Timing Path의 세트로 분해**
- **각 Path마다 신호 [[Propagation Delay]] 계산**
- **설계 내부 및 input/output 인터페이스 Timing Constraints Violation 확인**



## Tool

- Synopsys의 Primetime