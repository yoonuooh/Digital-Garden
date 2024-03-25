---
date: 2024-03-22
tags: VLSI
---

## 설명

- **Synthesis에 사용되고 Operating Condition을 위한 [[Cell]] 및 정의 포함**
	- 사용되는 [[Cell]]을 가지고 있는 Library → [[Link Library]]

> ([[Design Compiler User Guide.pdf#page=107&selection=8,49,9,75|Design Compiler User Guide, p.107]])
> Target libraries contain the cells used to generate the netlist and definitions for the design’s operating conditions.

> ([[Design Compiler User Guide.pdf#page=111&selection=69,0,71,28|Design Compiler User Guide, p.111]])
> Design Compiler selects functionally correct gates from the target libraries to build a circuit during mapping. It also calculates the timing of the circuit by using the vendor-supplied timing data for these gates.