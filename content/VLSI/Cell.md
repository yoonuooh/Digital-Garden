## 설명

- **설계에 여러 개의 [[Reference]]가 있을 수 있고 그 각각을 의미**
	- Instance라고도 함
	- 다른 Instance와 구분하기 위해 고유 이름을 가지고 있음

> ([[Design Compiler User Guide.pdf#page=48&selection=38,28,39,31|Design Compiler User Guide, p.48]])
> A design can contain multiple occurrences of a reference; each occurrence is an instance.

> ([[Design Compiler User Guide.pdf#page=49&selection=25,18,27,61|Design Compiler User Guide, p.49]])
> each instance has a unique name. A design can contain multiple instances; each instance points to the same reference but has a unique name to distinguish it from other instances. An instance is also known as a cell.



## [[Reference]]와 Cell의 관계

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