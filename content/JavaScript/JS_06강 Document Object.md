---
date: 2024-01-14
tags: JavaScript
---

## Document

- **HTML을 보여주는 object**
	- JavaScript와 HTML을 연결해주는 매개체
	- <span style="border-radius: 5px; color: black; background-color: salmon">document를 통해 HTML 정보를 조회하거나 수정할 수 있음</span>



## querySelector

- **element를 CSS 방식으로 검색**
	- 특정 class를 가진 요소의 하위 요소까지 검색 가능
	- <span style="color: orange"><u>조건을 만족하는 첫 번째 요소 하나만 출력</u></span>
		- 조건을 만족하는 모든 요소 출력 → `querySelectorAll()`
- `const title = document.querySelector("div.hello:first-child h1");`
	- class가 hello인 div 태그의 하위 첫 번째 h1 태그
- `const title = document.querySelector("#hello");`
	- id가 hello인 요소
	- `const title = document.getElementById("hello");`와 결과가 같음



## Event Listening

- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/HTMLHeadingElement)
- `addEventListener()`
	- 동작하는 함수명 뒤에 () 작성 금지
		- <span style="color: darkkhaki">()를 추가하면 조건이 만족하지 않아도 바로 함수를 실행</span>
- **특정 요소를 대상으로 사용 가능한 이벤트 조회**
	- `console.dir(element);`
	- "on~" 값인 경우 사용 가능

```js
const title = document.querySelector("div.hello:first-child h1");

function handleTitleClick() {
    title.style.color = "blue"; // JavaScript가 아니라 CSS로 style을 변경해야 적절함
}

function handleMouseEnter() {
    title.innerText = "Mouse is here.";
}

function handleMouseLeave() {
    title.innerText = "Mouse is gone.";
}

title.addEventListener("click", handleTitleClick);
title.addEventListener("mouseenter", handleMouseEnter);
title.addEventListener("mouseleave", handleMouseLeave);
```
