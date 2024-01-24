---
date: 2024-01-13
tags: JavaScript
---

## Function 선언

- **PHP와 유사**

```js
function sayHello(nameOfPerson, age) {
    console.log("Hello my name is " + nameOfPerson + " and I am " + age);
}

sayHello("A", 10);
sayHello("B", 20, 40, 50); // Error 발생하지 않음
sayHello("C", 30);
```



## Return

- **함수의 실행 결과를 반환**
	- <span style="border-radius: 5px; color: black; background-color: salmon">반환된 값을 다른 계산에 사용할 수 있음</span>
		- 함수의 실행 결과를 바로 출력할 때는 불가능
	- return 뒤 코드는 실행❌

```js
const calculator = {
    add: function (a, b) {
        return a + b;
    },
    minus: function (a, b) {
        return a - b;
    },
    multiply: function (a, b) {
        return a * b;
    },
    divide: function (a, b) {
        return a / b;
    },
    power: function (a, b) {
        return a ** b;
    },
}

const plusResult = calculator.add(4, 2) // 6
const minusResult = calculator.minus(plusResult, 2) // 4
const multiplyResult = calculator.multiply(4, minusResult) // 16
const divideResult = calculator.divide(multiplyResult, 2) // 8
const powerResult = calculator.power(divideResult, 2) // 64

console.log(powerResult);
```
