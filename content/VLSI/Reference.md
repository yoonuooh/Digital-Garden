## 설명

- **큰 회로를 만들 때 쓰이는 Library Component나 Design**
	- Design에 여러 개의 Reference가 포함될 수 있음
	- 같은 Reference이더라도 다른 Design의 Reference와 서로 무관

> ([[Design Compiler User Guide.pdf#page=48&selection=36,0,37,15|Design Compiler User Guide, p.48]])
> A reference is a library component or design that can be used as an element in building a larger circuit.

> ([[Design Compiler User Guide.pdf#page=49&selection=18,42,19,37|Design Compiler User Guide, p.49]])
> The references in one design are independent of the same references in a different design



## Reference와 [[Cell]]의 관계

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