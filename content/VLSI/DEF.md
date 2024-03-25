---
date: 2024-03-22
tags: VLSI
---

## 설명

- **설계의 Physical Layout을 표현하는 표준 Data 파일**
	- Physical Constraints
		- Floorplan Constraints
		- Powerplan Constraints
- **Floorplan Constraints를 사용하는 이유**
	- IP, Pad, Port의 Location 정보 없이 <span style="border-radius: 5px; color: black; background-color: khaki">임의로 배치한 다음 Optimization을 하면 비효율적이기 때문</span>
	- 정확하게 배치 공간을 표현하고 향후 PnR과 Timing 상관관계를 개선하기 위해서 사용
	- Physical 문제 예방
	- ECO가 힘듦
- **만드는 법**
	- IC Compiler의 Floorplan Data에 파생
	- 기존 DEF에서 추출
	- 수동으로 작성

> ([[Design Compiler User Guide.pdf#page=255&selection=19,0,21,6|Design Compiler User Guide, p.255]])
> The main reason to use floorplan constraints in topographical mode is to accurately represent the placement area and improve timing correlation with the post-place-and-route design

> ([[Design Compiler User Guide.pdf#page=255&selection=23,18,24,88|Design Compiler User Guide, p.255]])
> These physical constraints can be derived from IC Compiler floorplan data, extracted from an existing Design Exchange Format (DEF) file, or created manually.
