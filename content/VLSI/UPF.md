---
date: 2024-03-13
tags: VLSI
---

## 설명

- **설계자가 RTL과 함께 제공하는 Power Scenario**
	- 저전력 설계를 위해 고안
- **UPF 내용 예시**
	- 각 블록에 어떤 Power Rail이 연결되는지
	- 블록이 Power up이나 Shut down 되는 때
	- 다른 두 Power domain[^1] 사이에서 Voltage Level이 어떻게 이동하는지



## 구성

- Power Domains
- Power Supply Network
- Power State Table
- Isolation Strategies
- Retention Strategies
- Level Shifter Strategies
- Repeater Strategies

[^1]: 별도의 Power/Ground Network