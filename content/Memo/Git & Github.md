---
date: 2023-04-27
tags: Memo
tistoryBlogName: yoonuooh
tistoryTitle: Git & Github
tistoryTags: Memo
tistoryVisibility: "3"
tistoryCategory: "1154981"
tistorySkipModal: true
tistoryPostId: "2"
tistoryPostUrl: https://yoonuooh.tistory.com/2
---

## Git

- **설치**
	- CLI
		- Git bash
	- GUI
		- Sourcetree
		- 전체적인 branch 흐름을 확인하는 용도
- **초기 설정**
	- Git 전역으로 사용자 이름고 이메일 주소를 설정
		- `git config --global user.name "이름"`
		- `git config --global user.email "이메일"`
- **명령어**
	- 프로젝트 폴더를 VSCode로 열고 .git 폴더 생성
		- `git init`
		- <span style="color: salmon">.git 폴더가 없으면 Git 활용 불가</span>
	- Git 기록 확인
		- `git log`
		- J와 K로 창 스크롤
	- 폴더의 상황을 확인
		- `git status`
	- Git의 관리에서 특정 파일/폴더를 배제하는 경우 <span style="color: orange">.gitignore 사용</span>
		- .gitignore 파일 생성 → 배제하고 싶은 파일/폴더 입력
			- 파일 경로로 설정 가능
				- `/folder/file.c`
			- 특정 확장자 설정 가능
				- `*.c`
			- 예외 설정 가능
				- `!except.c`
			- 파일 또는 폴더와 그 내용들 설정 가능
				- `logs`
			- 폴더와 그 내용들 설정 가능
				- `logs/`
			- 폴더 안의 지정 파일 설정 가능
				- `logs/file.c`
- **프로젝트의 변경사항을 타임캡슐에 담기**
	- 파일 하나 담기
		- `git add file.c`
	- 파일 모두 담기
		- `git add .`
- **타임캡슐 묻기**
	- `git commit`
		- vi 에디터 진입
		- I 누르고 commit 메시지 입력
		- ESC → :wq → Enter
	- `git commit -m "First commit"`
		- commit 메시지와 함께 작성
	- `git commit -am "First commit"`
		- 파일 담기 및 commit 메시지 작성
- **과거로 돌아가기**
	- Reset
		- 과거로 돌아간 후 이후 기록은 삭제
		- `git reset --hard {commit 해시}`
		- commit 해시는 앞 몇 글자만 적어도 무방
		- commit 해시를 생략하면 마지막 commit을 의미
	- Revert
		- 작업 내용을 거꾸로 실행, 삭제 X
			- `git revert {commit 해시}`
- **branch**
	- branch 생성
		- `git branch {branch 이름}`
	- branch 조회
		- `git branch`
	- branch 전환
		- `git switch {branch 이름}`
	- branch 생성 및 전환
		- `git switch -c {branch 이름}`
	- branch 이름 변경
		- `git branch -m {branch 기존 이름} {branch 바꿀 이름}`
	- branch 삭제
		- `git branch -d {branch 이름}`
	- branch 합치기
		- merge
			- branch의 히스토리 포함
			- <span style="color: darkkhaki"><u>main branch에서</u></span> `git merge {합칠 branch 이름}`
		- rebase
			- 히스토리를 main에 포함
			- <span style="color: lightgreen"><u>합칠 branch에서</u></span> `git rebase main`
- **충돌 시 대처**
	- merge
		- branch 합치기 종료
			- `git merge --abort`
	- rebase
		- branch 합치기 종료
			- `git rebase --abort`
		- branch 합치기 재개
			- `git rebase --continue`
			- <span style="color: lightblue">rebase는 충돌이 여러 번 일어날 수 있기 때문</span>



## Github

- **토큰 발급 및 등록**
	- 발급
		- Github 프로필 → Settings → Developer settings → Personal access tokens → Generate new token
	- 등록
		- Window 자격 증명 관리자 → Window 자격 증명 → `git:https://@github.com` 자격 정보 생성 → 토큰 붙여넣기
- **협업 사용자 추가**
	- Repository 내 Settings → Collaborators → Manage access → Github ID나 E-mail 등록
- **초기 설정**
	- 로컬 Git 저장소에 원격 저장소로 연결 추가
		- `git remote add origin {원격 저장소 URL}`
	- 로컬 Git 저장소와 연결된 원격 저장소 목록 조회
		- `git remote`
		- `git remote -v`
	- 원격 저장소 삭제
		- `git remote rm origin`
	- 로컬 Git 저장소 commit 내역을 업로드
		- `git push -u origin main`
- **프로젝트 다운로드**
	- 미리 생성한 폴더에서 우클릭
	- Git bash here
	- `git clone {원격 저장소 URL}`
	- <span style="color: lightsteelblue">zip 설치와 달리 .git 폴더도 포함</span>
- **원격에 commit push**
	- 로컬의 변경사항을 원격으로 push
	- `git push`
- **원격의 commit pull**
	- 원격의 변경사항을 로컬로 pull
	- Github에서 간단한 수정 가능
	- `git pull`
- **원격의 변경사항이 반영되지 않은 로컬에서 수정한 후 push할 때 (충돌)**
	- `git push`를 입력해서 오류 확인
	- push할 것이 있을 때 pull하는 방법
		- merge 방식
			- `git pull --no-rebase`
		- rebase 방식
			- `git pull --rebase`
- **로컬 commit을 강제 push**
	- `git push --force`



> 출처 : [제대로 파는 Git & GitHub - 깃 끝.장.내.기 - 얄팍한 코딩사전](https://youtu.be/1I3hMwQU6GU)