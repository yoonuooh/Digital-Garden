---
date: 2024-01-13
tags: JavaScript
---

## Object

- **Python Class와 유사**
	- 변수와 함수를 포함할 수 있음
- **const는 Object에 해당**
	- Object를 수정하면 Error🚫
	- Object 속성 수정, 추가 가능
```js
const player = {
    name: "yoonuooh",
    points: 10,
    fat: true,
	sayHello: function(otherPersonName) {
        console.log("Hello " + otherPersonName);
    },
};

console.log(player);
player.fat = false;
console.log(player);

player.sayHello("A");
player.sayHello("B");
```
