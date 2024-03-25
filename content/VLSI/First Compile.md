---
date: 2024-03-22
tags: VLSI
---

## 설명

- **GTECH.v을 대상으로 Optimization 및 Synthesis**
	- <span style="color: salmon">Don't Touch Cell</span> → p.354
		- Tool이 임의로 <span style="color: salmon">Optimization하면 안되는 Cell</span>
	- <span style="color: orange">Don't Use Cell</span>
		- Power 등의 이유로 <span style="color: orange">Synthesis하면 안되는 Cell</span>
		- Synthesis 후에는 존재하지 않는 Cell
	- Optimization Technique
		- Cell의 VT 수정
		- Cell의 Drive Strength 수정
		- Logic Restructuring
		- Repeater 추가

> ([[Design Compiler User Guide.pdf#page=121&selection=62,0,67,7|Design Compiler User Guide, p.121]])
> When Design Compiler maps a design to a logic library, it selects library cells from this library. To specify cells in the target library to be excluded during optimization, use the set_dont_use command

![[Design Compiler User Guide.pdf#page=721&rect=68,178,475,335|Design Compiler User Guide, p.721]]