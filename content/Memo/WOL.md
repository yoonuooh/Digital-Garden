---
date: 2023-04-23
tags: Memo
tistoryBlogName: yoonuooh
tistoryTitle: WOL 설정 방법
tistoryTags: Memo
tistoryVisibility: "3"
tistoryCategory: "1155268"
tistorySkipModal: true
tistoryPostId: "3"
tistoryPostUrl: https://yoonuooh.tistory.com/3
---

## WOL 사용 조건

⚠️ <span style="border-radius: 5px; color: black; background-color: salmon">메인보드가 WOL, PCIe를 지원해야 함</span>
⚠️ <span style="border-radius: 5px; color: black; background-color: orange">컴퓨터가 사용하는 인터넷(공유기) 경로 파악</span>



## 바이오스 설정

- **부팅 후 ESC나 Del 연타**
	- 메인보드에 따라 다름
- **경로**
	- Advanced Option → PCIe 설정 Enable 및 Intel LAN 설정 Enable
	- 저장 후 재부팅



## 네트워크 어댑터 설정

- **고급**
	- 윈도우키 누르고 '장치 관리자' 검색
	- '네트워크 어댑터' 클릭
	- 'Intel Ehternet Connection' 우클릭 후 속성
	- '고급' 클릭
	- 'PME 활성화' ON, 'Wake on 매직 패킷' ON
- **전원 관리**
	- '전원 관리' 클릭
	- '전원을 절약하기 위해 컴퓨터가 이 장치를 끌 수 있음' OFF



## 공유기 설정

- **공유기를 통해 이더넷으로 사용하는 경우**
	- 공유기 관리 페이지에 접속
		- 192.168.0.1
	- Wake on LAN 설정에서 컴퓨터의 Mac 주소 등록
	- 원격제어 설정에서 4자리 숫자 등록
		- 외부에서 공유기 설정 페이지에 들어갈 때 사용함
	- 외부 기기에서 공유기의 '외부 IP:4자리 숫자'를 웹사이트에 검색
		- Ex) <span style="border-radius: 5px; color: black; background-color: khaki">111.111.111.111:4444</span>
		- 외부에서 공유기 설정 페이지 접속되는지 확인
		- 외부 IP는 공유기 설정 페이지에서 확인 가능



## 윈도우 전원 옵션

- **경로**
	- 제어판 → 하드웨어 및 소리 → 전원 옵션 → 전원 단추 작동 설정 → 빠른 시작 켜기 OFF
		- '현재 사용할 수 없는 설정 변경'을 누르면 OFF 가능