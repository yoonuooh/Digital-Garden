---
date: 2024-03-22
tags: VLSI
---

## 설명

- **RTL Syntax Error Check**
	- HDL Source 파일 읽음
	- 설계에 Generic Logic을 만들지 않고 Error Check
	- HDL과 무관한 중간 Format으로 HDL Library Object를 만듦
- **Error가 발생하면**
	- HDL Source를 수정
	- 다시 `analyze` 실행
- **Analyze가 완료되면**
	- 이후로는 Design을 수정했을 때만 다시 Analyze

> ([[Design Compiler User Guide.pdf#page=151&selection=125,0,125,24|Design Compiler User Guide, p.151]])
> Reads an HDL source file

> ([[Design Compiler User Guide.pdf#page=151&selection=128,0,128,63|Design Compiler User Guide, p.151]])
> Checks for errors without building generic logic for the design

> ([[Design Compiler User Guide.pdf#page=151&selection=131,0,131,69|Design Compiler User Guide, p.151]])
> Creates HDL library objects in an HDL-independent intermediate format

> ([[Design Compiler User Guide.pdf#page=152&selection=21,0,29,13|Design Compiler User Guide, p.152]])
> If the analyze command reports errors, fix them in the HDL source file and then run the analyze command again

> ([[Design Compiler User Guide.pdf#page=152&selection=29,15,30,9|Design Compiler User Guide, p.152]])
> After a design is analyzed, you must reanalyze it only when you change it
