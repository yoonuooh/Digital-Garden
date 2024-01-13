---
date: 2024-01-09
tags: Linux
---

## 설치 방법

- **Debian 설치**
	- `proot-distro install debian`
- **Debian 접속 및 업데이트**
	- `proot-distro login debian`
	- `apt update && apt upgrade`
- **wget 설치**
	- `apt install wget`
- **code-server 설치**
	- [code-server github](https://github.com/coder/code-server)에서 최신 Release의 arm64.tar.gz로 설치
	- `wget https://github.com/coder/code-server/releases/download/v4.20.0/code-server-4.20.0-linux-arm64.tar.gz`
	- `tar -xvf code-server-4.20.0-linux-arm64.tar.gz`



## 실행 방법

- **code-server/bin 폴더 내 code-server 실행**
	- `./code-server --auth none --host 0.0.0.0`
		- 비밀번호 설정 X
		- localhost

> 출처 : [@baealex 블로그](https://blex.me/@baealex/development-environment-within-android)