---
date: 2024-03-10
tags: VLSI
---

## 설명

- **RTL 코드를 읽고 설계를 최적화해서 합성 Netlist를 만드는 과정**
    - Translation
    - Optimization
    - Mapping
        - RTL code에 명시된 기능을 표준 셀 라이브러리로 매핑

> ([[Design Compiler User Guide.pdf#page=47&selection=26,52,27,72|Design Compiler User Guide, p.47]])
> Synthesis includes reading the HDL source code and optimizing the design created from that description.



## Input / Output

- **Input**
    - RTL
    - .db
    - [[SDC]]
    - [[UPF]]
- **Output**
    - 합성 Netlist
    - SVF
    - SDC
    - Report



## [[RTL Synthesis Flow]]



## Tool

- Synopsys의 [[Design Compiler]]
- Synopsys의 Fusion Compiler



## 정보

- **RTL Synthesis 스텝을 DC, DCG, FC라고 표현**
    - 보통 스텝에 해당하는 툴 이름으로 스텝을 표현
    - DCG (Design Compiler Graphical)
        - Floorplan 정보([[DEF]])를 기반으로 합성했을 때
- **Synthesis할 때 UPF와 SDC를 입력하는 이유**
    - [[UPF]]
        - 설계 과정에서 Power Intent를 명시하기 위해
    - [[SDC]]
        - 정확한 Timing 분석
        - Timing Constraints를 명시해서 설계의 Timing 요건을 만족하고 Timing Violation을 방지
- **Synthesis할 때 UPF와 SDC가 반드시 필요한가?**
    - RTL은 Power 정보와 Timing 정보가 없고 기능 정보만 있음
    - RTL이 없어도 Synthesis는 가능하지만 Optimization 불가