---
date: 2023-11-30
tags: Linux
---

## openssh

- **터미널 환경에서 다른 PC에 IP를 통해 접속하게 해주는 프로그램 (Putty와 유사)**
	- 설치
		- Termux
			- `pkg install openssh`
	- 원격 PC 접속
		- `ssh {username}@{IP} -p {Port}`



## scp

- **터미널 환경에서 다른 PC에 IP를 통해 파일을 복사해서 전송하는 프로그램**
	- 로컬 → 원격
		- 디렉토리 내 모든 파일/디렉토리 복사
			- `scp -r {로컬 디렉토리} {username}@{IP}:{원격에서 받는 경로}`
		- 지정 포트로 복사
			- `scp -P {Port} {로컬 파일} {username}@{IP}:{원격에서 받는 경로}`
		- 파일 여러 개 복사
			- `scp {파일 1} {파일 2} {username}@{IP}:{원격에서 받는 경로}`
	- 원격 → 로컬
		- 디렉토리 내 모든 파일/디렉토리 복사
			- `scp -r {username}@{IP}:{원격 디렉토리} {로컬에서 받는 경로}`
		- 지정 포트로 복사
			- `scp -P {Port} {username}@{IP}:{원격 파일} {로컬에서 받는 경로}`
		- 파일 여러 개 복사
			- `scp {username}@{IP}:"{파일 1} {파일 2}" {로컬에서 받는 경로}`
				- <span style="border-radius: 5px; color: black; background-color: khaki">★ 큰따옴표(" ")로 묶어야 함</span>