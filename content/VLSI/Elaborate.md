---
date: 2024-03-22
tags: VLSI
---

## 설명

- **Design을 GTECH.v으로 변환**
	- GTECH.v
		- 연결 정보만 존재
		- Drive Strength, Cell Type 없이 Ideal하게 연결된 상태
- **HDL의 산술 연산자를 [[DesignWare Library]]의 Components로 대체**
- **자동으로 [[Linking Design]] 실행**

> ([[Design Compiler User Guide.pdf#page=152&selection=38,0,39,43|Design Compiler User Guide, p.152]])
> Translates the design into a technology-independent design (GTECH) from the intermediate files produced during analysis

> ([[Design Compiler User Guide.pdf#page=152&selection=48,0,48,76|Design Compiler User Guide, p.152]])
> Replaces the HDL arithmetic operators in the code with DesignWare components

> ([[Design Compiler User Guide.pdf#page=152&selection=51,0,55,41|Design Compiler User Guide, p.152]])
> Automatically executes the link command, which resolves design references