---
date: 2024-03-22
tags: VLSI
---

## 설명

- **Scan.v을 대상으로 Optimization 및 Synthesis**
	- [[DFT]], Timing 수정, Netlist 수정 등 과정을 거친 후 1번 더 Optimization 및 Synthesis
	- [[First Compile]] 이후에 설계의 구조를 향상시킴으로써 결과를 개선할 수 있음

> ([[Design Compiler User Guide.pdf#page=337&selection=71,0,73,66|Design Compiler User Guide, p.337]])
> In topographical mode, you can perform a second-pass, incremental compile to enable topographical-based optimization for post-topographical-based synthesis flows such as retiming, design-for-test (DFT), DFTMAX, and minor netlist edits. 

> ([[Design Compiler User Guide.pdf#page=337&selection=29,31,30,64|Design Compiler User Guide, p.337]])
> Design Compiler can improve quality of results (QoR) by improving the structure of your design after the initial compile