---
date: 2023-11-22
tags:
  - 자동제어실험
cssclasses:
  - purpleRed
---

## 폐루프 시스템

- **실험 내용**
	- 입력 전압 : 1V 펄스파, 주파수 500Hz
	- 폐루프 시스템 구성 요소 확인
		- 차동증폭기
		- 전달함수 회로
		- 전원 팔로워(버퍼)
	- 상승시간, 정상상태오차 확인
		- 시뮬레이션
			- 상승시간 $T_r = 112.83 \mu s$
			- 정상상태오차 $e_{ss} = 0.50V$
		- 실험
			- 상승시간 $T_r = 105 \mu s$
			- 정상상태오차 $e_{ss} = 0.47V$

![폐루프 시스템 회로](https://user-images.githubusercontent.com/128121919/284821288-f7dd6fef-1c98-4d02-8e95-276039708403.png)![폐루프 시스템 결과](https://user-images.githubusercontent.com/128121919/284821282-968ec75a-93e1-42e6-9565-4935896df87e.png)



## P 제어 시스템

- **실험 내용**
	- 입력 전압 : 1V 펄스파, 주파수 500Hz
	- 상승시간, 정상상태 오차 확인
	- 제어 이득 $K_P$를 2배, 5배로 변화시키며 결과 확인
		- 무엇이 향상되었는가?
			- 상승 시간과 정상상태오차가 일부 감소했다.

![P 제어 시스템 1 회로](https://user-images.githubusercontent.com/128121919/284821257-296e27be-3257-4ef2-b963-236c58a73e45.png)![P 제어 시스템 1 결과](https://user-images.githubusercontent.com/128121919/284821248-52eaff45-d055-41fa-9ac1-570fa79239e5.png)

![P 제어 시스템 2 회로](https://user-images.githubusercontent.com/128121919/284821263-3a902895-2538-4326-a83e-dfada2378ed8.png)![P 제어 시스템 2 결과](https://user-images.githubusercontent.com/128121919/284821260-df00b99c-8eb8-4f01-ab38-bcdefb700a6d.png)

![P 제어 시스템 3 회로](https://user-images.githubusercontent.com/128121919/284821271-823ddea5-a708-46a9-867c-522c3d636432.png)![P 제어 시스템 3 결과](https://user-images.githubusercontent.com/128121919/284821267-f56b3b8f-c9d3-4960-a0b9-164ab97b566d.png)

| P 제어 시스템 | 상승시간 | 정상상태오차 |
|:-------------:|:--------:|:------------:|
| 제어 이득 = 1 (시뮬레이션) | 112.83μs |    0.50V     |
| 제어 이득 = 2 (시뮬레이션) | 71.92μs  |    0.33V     |
| 제어 이득 = 5 (시뮬레이션) | 35.24μs  | 0.17V             |



## PD 제어 시스템

- **실험 내용**
	- 입력 전압 : 1V 펄스파, 주파수 500Hz
	- 상승시간, 정상상태 오차 확인
		- 시뮬레이션
			- 상승시간 $T_r = 2.71 \mu s$
			- 정상상태오차 $e_{ss} = 0.50V$
	- 기존의 결과와 비교하여 무엇이 향상되었는가?
		- 상승시간이 상당히 많이 감소했다.

![PD 제어 시스템 회로](https://user-images.githubusercontent.com/128121919/284821277-1f1e5651-7e9c-4b1b-a73b-ac1b4ddc0653.png)![PD 제어 시스템 결과](https://user-images.githubusercontent.com/128121919/284821273-f5b1f797-a5af-4534-b6d3-a94cce82eec9.png)



## PI 제어 시스템

- **실험 내용**
	- 입력 전압 : 1V 펄스파, 주파수 500Hz
	- 상승시간, 정상상태 오차 확인
		- 시뮬레이션
			- 상승시간 $T_r = 216.90 \mu s$
			- 정상상태오차 $e_{ss} = 0V$
	- 기존의 결과와 비교하여 무엇이 향상되었는가?
		- 상승시간은 2배 증가했으나 정상상태오차가 0이 됐다.

![PI 제어 시스템 회로](https://user-images.githubusercontent.com/128121919/284821281-06fe854b-1a9b-4799-9d03-aeaa1fae6ac6.png)![PI 제어 시스템 결과](https://user-images.githubusercontent.com/128121919/284821280-65690d50-b4b2-4755-a8a1-32547db6d263.png)