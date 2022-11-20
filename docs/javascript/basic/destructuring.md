---
layout: default
title: 구조분해할당
grand_parent: 자바스크립트
parent: 자바스크립트 기초
has_children: false
permalink: /docs/javascript/destructuring
nav_order: 2
---


### **구조분해할당**

객체나 배열을 변수로 분해 할수 있게 해주는 문법



#### **구조분해할당 기본 형식**

```js
const numbers = [1, 2]
const [num1, num2] =  numbers;

console.log(num1); //1
console.log(num2); //2
```




#### **구조분해할당 + 중복배열**

```js
const numbers = [1, 2, [3, 4], 5];
const [num1, num2] =  numbers;

console.log(num1); //1
console.log(num2); //2
console.log(num3); //[ 3, 4 ]
console.log(num4); //5
console.log(num5); //undefined
```


#### **구조분해할당 + 나머지 패턴**

```js
const numbers = [1, 2, 3, 4, 5]
const [num1, num2, ...num3] =  numbers;

console.log(num1); //1
console.log(num2); //2
console.log(num3); //[3, 4, 5]
```

#### **객체 분해 + 변수**

```js
let person = {
    name: "kim",
}

let {name:nickname, age, weight} = person;
console.log(nickname); //kim
```

### **참고**
> [모던 JavaScript 튜토리얼 - 구조 분해 할당](https://ko.javascript.info/destructuring-assignment){:target="_blank"}  
  


