---
date: 2024-01-14
tags: JavaScript
---

## Style 변경

- **JavaScript로 Style을 변경하는 것은 적절하지 않음**
	- JavaScript는 Style 변경하는 도구가 아님
	- Style 정보는 CSS에 모음

```js
const h1 = document.querySelector("div.hello:first-child h1");

function handleTitleClick () {
    const currentColor = h1.style.color;
    let newColor;

    if (currentColor === "lightsteelblue") {
        newColor = "salmon";
    }
    else {
        newColor = "lightsteelblue";
    }
    h1.style.color = newColor;
}

h1.addEventListener("click", handleTitleClick);
```



## className

- **JavaScript로 태그의 class를 업데이트해서 style 변경**
```css
body {
    background-color: beige;
}

h1 {
    color: lightsteelblue;
}

.clicked {
    color: salmon;
}

.good-font {
    font-family: 'Courier New', Courier, monospace;
}
```

```js
const h1 = document.querySelector("div.hello:first-child h1");

function handleTitleClick () {
    const clickedClass = "clicked";

    if (h1.className === clickedClass) {
        h1.className = "";
    }
    else {
        h1.className = clickedClass;
    }
}

h1.addEventListener("click", handleTitleClick);
```

> [!info]+
> - 위 코드는 기존에 존재하는 className을 저장하지 않음
> - "clicked"가 "good-font"를 대체하여 <span style="color: salmon">"good-font" 소실</span>
> - 이를 방지하기 위해 classList 사용



## classList

- **여러 className을 추가, 수정, 삭제할 때 사용**
	- contains()
	- remove()
	- add()
	- toggle()
		- <span style="color: orange">toggle()로 contains(), remove(), add() 대체 가능</span>

```js
const h1 = document.querySelector("div.hello:first-child h1");

function handleTitleClick () {
    const clickedClass = "clicked";

    if (h1.classList.contains(clickedClass)) {
        h1.classList.remove(clickedClass)
    }
    else {
        h1.classList.add(clickedClass)
    }
}

h1.addEventListener("click", handleTitleClick);
```

$$\downarrow$$

```js
const h1 = document.querySelector("div.hello:first-child h1");

function handleTitleClick () {
    h1.classList.toggle("clicked");
}

h1.addEventListener("click", handleTitleClick);
```
