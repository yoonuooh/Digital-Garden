---
date: 2024-03-22
tags: VLSI
---

## 설명

- **Design Compiler가 Cell Instance와 Reference를 연결하는데 사용하는 Logic Library**
	- 모든 Cell Instance와 Library Component를 연결할 때 사용
	- Timing과 Path Delay를 계산하는데 사용되는 Delay 정보 등 포함

> ([[Design Compiler User Guide.pdf#page=110&selection=53,0,54,10|Design Compiler User Guide, p.110]])
> The logic libraries that Design Compiler uses to resolve cell references are called link libraries.

> ([[Design Compiler User Guide.pdf#page=107&selection=10,85,11,90|Design Compiler User Guide, p.107]])
> Link libraries define the delay models that are used to calculate timing values and path delays