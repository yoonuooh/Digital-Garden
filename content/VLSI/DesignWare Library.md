---
date: 2024-03-22
tags: VLSI
---

## 설명

- **Synopsys Synthesis 환경에서 만들어진 Reusable Block을 모아놓은 Library**
	- Synthesis 중 [[Design Compiler]]는 DesignWare Library에서 최적의 Component를 선택
	- 산술 연산자와 조건문 등 구현

> ([[Design Compiler User Guide.pdf#page=113&selection=23,0,26,18|Design Compiler User Guide, p.113]])
> A DesignWare library is a collection of reusable circuit-design building blocks (components) that are tightly integrated into the Synopsys synthesis environment. During synthesis, Design Compiler selects the component with the best speed and area optimization from the DesignWare library

> ([[Design Compiler User Guide.pdf#page=113&selection=27,0,29,16|Design Compiler User Guide, p.113]])
> DesignWare components that implement many of the built-in HDL operators are provided by Synopsys. These operators include +, -, *, <, >, <=, >=, and the operations defined by if and case statements.
