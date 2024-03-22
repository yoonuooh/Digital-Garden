---
date: 2024-03-20
tags: VLSI
---

## 설명

- **Synopsys의 command, attribute, constraint는 Design Object를 지향함**



## Reference

- **큰 회로를 만들 때 쓰이는 Library Component나 Design**
	- Design에 여러 개의 Reference가 포함될 수 있음
	- 같은 Reference이더라도 다른 Design이면 서로 무관

> ([[Design Compiler User Guide.pdf#page=48&selection=36,0,37,15|Design Compiler User Guide, p.48]])
> A reference is a library component or design that can be used as an element in building a larger circuit.

> ([[Design Compiler User Guide.pdf#page=49&selection=18,42,19,37|Design Compiler User Guide, p.49]])
> The references in one design are independent of the same references in a different design



## Instance (Cell)

- **Reference에 붙인 고유 이름**
	- 다른 Instance와 구분됨

> ([[Design Compiler User Guide.pdf#page=49&selection=25,18,27,61|Design Compiler User Guide, p.49]])
> each instance has a unique name. A design can contain multiple instances; each instance points to the same reference but has a unique name to distinguish it from other instances. An instance is also known as a cell.



## Port

- **Design(상위 Hierarchy)의 Input과 Output**

> ([[Design Compiler User Guide.pdf#page=49&selection=36,0,37,16|Design Compiler User Guide, p.49]])
> Ports are the inputs and outputs of a design. The port direction is designated as input, output, or inout



## Pin

- **Cell(하위 Hierarchy)의 Input과 Output**
	- Subdesign의 Port는 Parent Design 기준으로 Pin

> ([[Design Compiler User Guide.pdf#page=49&selection=41,0,42,49|Design Compiler User Guide, p.49]])
> Pins are the input and output of cells (such as gates and flip-flops) within a design. The ports of a subdesign are pins within the parent design.



## Net

- **Port ↔ Pin, Pin ↔ Pin을 연결한 선**

> ([[Design Compiler User Guide.pdf#page=49&selection=46,0,46,68|Design Compiler User Guide, p.49]])
> Nets are the wires that connect ports to pins and pins to each other



![[Design Compiler User Guide.pdf#page=48&rect=71,293,523,634|Design Compiler User Guide, p.48]]



## Example

![[Design Compiler User Guide.pdf#page=50&rect=66,480,490,665|Design Compiler User Guide, p.50]]

- **Reference**
	- NAND2
	- MULTIPLIER
- **Instance**
	- NAND2
		- U1
		- U2
		- U3
	- MULTIPLIER
		- U4

> ([[Design Compiler User Guide.pdf#page=50&selection=26,0,27,65|Design Compiler User Guide, p.50]])
> The EXREF design contains two references: NAND2 and MULTIPLIER. NAND2 is instantiated three times, and MULTIPLIER is instantiated one time

> ([[Design Compiler User Guide.pdf#page=50&selection=28,0,30,17|Design Compiler User Guide, p.50]])
> The names given to the three instances of NAND2 are U1, U2, and U3. The references of NAND2 and MULTIPLIER in the EXREF design are independent of the same references in different designs
