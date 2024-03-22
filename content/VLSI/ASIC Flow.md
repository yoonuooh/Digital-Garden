---
date: 2024-03-11
tags: VLSI
---

## [[RTL Synthesis]]


![[RTL Synthesis#Input / Output]]



## [[Pre-Sanity Check]]

- **[[EQ Check]]**
![[EQ Check#Input / Output]]

- **[[LP Check]]**
![[LP Check#Input / Output]]

- **[[LDRC]]**
![[LDRC#Input / Output]]

- **[[STA]]**
![[STA#Input / Output]]



## [[DFT]]



## Pre-Sanity Check



## Floorplan

- **IP와 I/O Pad를 배치하고 Standard Cell row를 생성하는 과정**
    - PI에서 Netlist, UPF, SDC를 전달받음



## Powerplan

- **Mesh 형태로 Power 배치하는 과정**
    - Macro, Standard Cell 등에 전력 공급



## Place

- **Standard Cell을 배치하는 과정**
    - 각 셀마다 적절한 물리적 위치를 찾는 과정



## CTS

- **Flip-Flop의 [[Clock Skew]]를 0으로 만드는 과정**



## Route

- **Metal Layer를 사용해 물리적으로 Pin을 연결하는 과정**



## Chip Finish

- **Standard Cell 사이를 Filler Cell로 채우는 과정**
    - Finish Net 출력



## [[Post-Sanity Check]]

- **[[EQ Check]]**
![[EQ Check#Input / Output]]

- **[[LP Check]]**
![[LP Check#Input / Output]]

- **[[LDRC]]**
![[LDRC#Input / Output]]

- **[[STA]]**
![[STA#Input / Output]]



## ECO

- **Finish Net을 대상으로 Timing Violation을 해결하는 과정**



![[ASIC Flow.drawio.png]]
