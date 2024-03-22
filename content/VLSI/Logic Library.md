---
date: 2024-03-22
tags: VLSI
---

## 설명

- **Operating Condition 정의**
	- PVT
		- (Manufacture) Process
		- Voltage
		- Temperature
	- Maximum Transition Time
	- WLM
- **사용 이유**
	- 설계 기능 구현
		- <span style="color: salmon">Target Library</span>
	- Cell Reference 해결
		- <span style="color: orange">Link Library</span>
	- Timing, Path Delay 계산
		- <span style="color: orange">Link Library</span>
	- 전력 소모 계산

> ([[Design Compiler User Guide.pdf#page=110&selection=20,0,22,42|Design Compiler User Guide, p.110]])
> Logic libraries, which are maintained and distributed by semiconductor vendors, contain information about the characteristics and functions of each cell, such as cell names, pin names, area, delay arcs, and pin loading. 

> ([[Design Compiler User Guide.pdf#page=110&selection=23,13,25,33|Design Compiler User Guide, p.110]])
> the maximum transition time for nets. These conditions are called design rule constraints. In addition, a logic library specifies the operating conditions and wire load models for a specific technology.