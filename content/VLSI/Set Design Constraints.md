---
date: 2024-03-22
tags: VLSI
---

## 설명

- **Design Rule Constraints**
	- Function이 의도한대로 작동하기 위해 반드시 만족해야 하는 제한 사항
	- [[Logic Library]]에서 정의
	- [[MTT]], Maximum Fanout 등
- **Optimization Constraints**
	- Speed, Area, Power 목표
	- 중요하지는 않지만 원하는 제한 사항
	- Input/Output Delay, Maximum Area, Power Optimization 등

> ([[Design Compiler User Guide.pdf#page=213&selection=34,0,35,21|Design Compiler User Guide, p.213]])
> Design rule constraints reflect technology-specific restrictions that your design must meet to function as intended.

> ([[Design Compiler User Guide.pdf#page=212&selection=24,0,25,28|Design Compiler User Guide, p.212]])
> The logic library defines these implicit constraints. These constraints are required for a design to function correctly

> ([[Design Compiler User Guide.pdf#page=226&selection=58,0,59,73|Design Compiler User Guide, p.226]])
> Optimization constraints represent speed, area, and power design goals and restrictions that you want but that might not be crucial to the operation of a design.