---
date: 2024-03-14
tags: VLSI
---

## 설명

- **Setup Time 또는 Hold Time을 만족하는 기준 시간**
	- <span style="color: salmon">Setup Required Time</span>
		- $t_{laun} + T - t_{setup}$
			- <span style="border-radius: 5px; color: black; background-color: salmon">Setup Time만큼 앞선 시각까지</span>
		- <u>Clock의 주파수가 커지면</u>
			-  $T$ 감소
			- Setup Required Time 감소
			- Setup Slack 감소
	- <span style="color: orange">Hold Required Time</span>
		- $t_{laun} + t_{hold}$
			- <span style="border-radius: 5px; color: black; background-color: orange">Hold Time만큼 뒤진 시각부터</span>
		- <u>Clock의 주파수와 무관</u>
- **[[Setup Time]] 만족 조건**
	- Setup Required Time > [[Arrival Time]]
	- <span style="color: darkkhaki">Setup Slack</span>
		- <span style="color: darkkhaki">Setup Required Time - Arrival Time</span>
- **[[Hold Time]] 만족 조건**
	- Hold Required Time < Arrival Time
	- <span style="color: lightgreen">Hold Slack</span>
		- <span style="color: lightgreen">Arrival Time - Hold Required Time</span>

![Arrival Time](https://qph.cf2.quoracdn.net/main-qimg-a671d5e8ec3ea10496292c5d68b6537b)

![Setup Time](https://qph.cf2.quoracdn.net/main-qimg-a82305103fac294f787834ef36091ab9)

[^1]: Setup Required Time - Arrival Time