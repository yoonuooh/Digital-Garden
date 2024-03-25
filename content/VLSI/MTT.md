---
date: 2024-03-14
tags: VLSI
---

## 설명

- **[[Net]]의 Max [[Transition Time]]**
	- Driving Pin의 논리값이 변할 때 필요한 최대 시간
	- 많은 [[Logic Library]]에 [[Pin]]의 MTT가 포함되어 있음

> ([[Design Compiler User Guide.pdf#page=214&selection=64,0,65,72|Design Compiler User Guide, p.214]])
> Maximum transition time is a design rule constraint. The maximum transition time for a net is the longest time required for its driving pin to change logic values.

> ([[Design Compiler User Guide.pdf#page=214&selection=65,73,67,41|Design Compiler User Guide, p.214]])
> Many logic libraries contain restrictions on the maximum transition time for a pin, creating an implicit transition time limit for designs using that library



## MTTV