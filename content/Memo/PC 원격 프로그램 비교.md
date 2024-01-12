---
date: 2023-11-26
tags: Memo
cssClass: purpleRed, wideTable
tistoryBlogName: yoonuooh
tistoryTitle: PC 원격 프로그램 비교
tistoryTags: Memo
tistoryVisibility: "3"
tistoryCategory: "1155268"
tistorySkipModal: true
tistoryPostId: "8"
tistoryPostUrl: https://yoonuooh.tistory.com/8
---

갤럭시탭만 가지고 다니다가 갑자기 PC가 필요할 때가 있었습니다.
이전까지는 그럴 때마다 [Parsec](https://parsec.app/)이라는 앱을 사용했는데 갤럭시탭 정품 키보드커버 트랙패드로 작업하기에 불편함이 있었습니다.
그래서 [Moonlight](https://moonlight-stream.org/)와 [SuperDisplay (Beta)](https://superdisplay.app/)에 대해서 몇 가지를 알아봤고 원격 프로그램을 알아보고 있는 분들께 도움이 될 것 같아 글을 써봅니다.



## Moonlight

<span style="border-radius: 5px; color: black; background-color: salmon">Moonlight는 게임 스트리밍 프로그램</span>입니다.
원격 PC에 접속하면 게임을 바로 실행하게 되어있지만 실행하는 <span style="color: salmon">mstsc.exe</span> 파일을 시작 프로그램으로 설정할 수 있습니다.
이렇게 하면 아무 프로그램을 실행하지 않은 것과 같고 바탕화면에서 시작합니다.

이전에는 NVIDIA 그래픽카드가 있는 PC에서만 사용할 수 있었습니다.
최근에는 [Sunshine](https://github.com/LizardByte/Sunshine)이라는 프로그램을 통해 모든 PC에서 사용할 수 있게 바뀌었습니다.

- **장점**
	- 빠른 속도, 적은 지연율
	- 고화질, 고해상도(120Hz)
- **단점**
	- 어려운 설정 난이도
		- 외부(다른 인터넷 망)에서 사용하는 것이 아니어도 공유기 포트포워딩 설정[^1] 필수
		- Sunshine 프로그램이 나오면서 난이도가 약간 쉬워짐
	- 원격 PC에 접속하는 시간이 상대적으로 오래 걸림



## Parsec

<span style="border-radius: 5px; color: black; background-color: orange">Parsec은 게임 스트리밍 프로그램</span>입니다.
계정이 필요없고 원격 PC의 IP로 접속하는 Moonlight와 달리 Parsec은 계정을 통해 접속하는 방식입니다.
기기 사이에 Parsec 회사가 개입한다고 생각하면 되고 이게 보안상 좋은 건지 나쁜 건지는 모르겠습니다.

- **장점**
	- 쉬운 설정 난이도
		- <span style="color: orange">회원가입만 하면 OK</span>
	- 원격 PC에 접속하는 시간이 빠름
- **단점**
	- Moonlight에 비해 지연율이 크고 화질이 떨어짐
	- 새로운 환경(인터넷 망)에서 원격 PC에 접속할 때마다 Parsec 로그인 시 이메일 인증을 해야함
		- 보안에 신경쓰는 것은 이해하나 불편함



## SuperDisplay (Beta)

<span style="border-radius: 5px; color: black; background-color: khaki">SuperDisplay는 안드로이드 모니터 확장 유료앱입니다.</span>
원래 안드로이드 기기를 다른 기기에 연결하여 화면을 복제하거나 확장해서 포터블 모니터나 타블렛[^2] 역할로 쓰는 앱입니다.
SuperDisplay (Beta) 버전이 나오면서 IP를 통해 원격으로 다른 PC에 접속하는 기능이 생겨서 원격 프로그램으로도 쓸 수 있습니다.

❗ [플레이스토어](https://play.google.com/store/apps/datasafety?id=com.kelocube.mirrorclient&pli=1)에서 베타 테스터 신청을 한 상태에서 원격 접속을 할 수 있습니다.

- **장점**
	- 원격 PC에 접속하는 시간이 빠름
	- 터치 환경에서는 다른 프로그램에 비해 상대적으로 편리
		- 윈도우의 태블릿 모드를 사용한다면 키보드, 마우스가 없을 때 사용할 만함
- **단점**
	- 유료
		- <span style="color: darkkhaki">플레이스토어에서 15달러</span>
			- 설치 후 3일 간은 모든 기능 무료
	- 외부에서 접속하려면 포트포워딩 설정[^3] 필요
		- Moonlight에 비교하면 간단한 편
	- 트랙패드 사용 시 마우스 스크롤을 할 때 확대/축소가 같이 동작
		- 웹 서핑 시 이 점이 매우 불편해서 트랙패드로는 사용하지 못할 정도



## 마무리

전체적인 만족도는 <span style="border-radius: 5px; color: black; background-color: lightgreen">Moonlight > Parsec > SuperDisplay (Beta)</span> 였습니다.

프로그램마다 간단하게 웹 서핑을 해보면서 테스트해본 결과로 갤럭시탭 S7+ 정품 키보드커버 트랙패드 기준입니다.
'트랙패드 클릭'은 물리적으로 트랙패드를 누르는 것을 의미합니다.
훗날 프로그램이 업데이트되면 표 내용이 틀릴 수 있습니다. (2023-11-30 기준)

|   원격 앱 비교    |                   Moonlight                   |              Parsec               |    SuperDisplay (Beta)    |
|:-----------------:|:---------------------------------------------:|:---------------------------------:|:-------------------------:|
|   마우스 좌클릭   |            트랙패드 한 손가락 터치            |      트랙패드 한 손가락 클릭      |  트랙패드 한 손가락 터치  |
|   마우스 우클릭   |            트랙패드 두 손가락 터치            |      트랙패드 두 손가락 터치      |    화면 두 손가락 터치    |
|   마우스 드래그   | 트랙패드 한 손가락 롱터치 OR 두 손가락 드래그 | 트랙패드 한 손가락 클릭 후 드래그 |     트랙패드로 불가능     |
|   마우스 스크롤   |             화면 두 손가락 스크롤             |       화면 두 손가락 스크롤       | 트랙패드 두 손가락 스크롤 |
| 원격 PC Alt + Tab |                       O                       |                 X                 |             X             |
| 원격 PC Window 키 |                       O                       |                 X                 |             X             |

[^1]: 다른 인터넷 망에서 원격 PC에 접속하는 포트포워딩 외 Moonlight 자체적으로 필요한 포트포워딩
[^2]: 갤럭시탭 S펜 사용 가능하고 필압 지원
[^3]: 다른 인터넷 망에서 원격 PC에 접속하는 포트포워딩