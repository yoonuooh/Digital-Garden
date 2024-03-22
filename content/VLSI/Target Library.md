---
date: 2024-03-22
tags: VLSI
---

## 설명

- **Design Compiler가 Optimization 중에 Mapping하는 Logic Library**
	- Netlist를 만들 때 사용되는 Cell 포함
	- Operating Condition 포함

> ([[Design Compiler User Guide.pdf#page=110&selection=41,0,42,10|Design Compiler User Guide, p.110]])
> The logic libraries that Design Compiler maps to during optimization are called target libraries.

> ([[Design Compiler User Guide.pdf#page=107&selection=8,49,10,83|Design Compiler User Guide, p.107]])
> Target libraries contain the cells used to generate the netlist and definitions for the design’s operating conditions. The target libraries are the subset of the link libraries that are used to compile or translate a design

> ([[Design Compiler User Guide.pdf#page=111&selection=69,0,71,28|Design Compiler User Guide, p.111]])
> Design Compiler selects functionally correct gates from the target libraries to build a circuit during mapping. It also calculates the timing of the circuit by using the vendor-supplied timing data for these gates.