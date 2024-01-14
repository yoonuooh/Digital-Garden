---
date: 2024-01-13
tags: JavaScript
---

## if - else if - else

- **if구문, 논리 연산자가 C와 같음**
```js
const age = parseInt(prompt("How old are you?")); // == int(input()) in Python

if (isNaN(age) || age < 0) {
    console.log("Write a positive number.");
}
else if (age < 18) {
    console.log("You are too young.");
}
else if (age >= 18 && age <= 50) {
    console.log("You can drink.");
}
else if (age === 100) {
    console.log("Good.")
}
else {
    console.log("You have to stop drinking.");
}
```
