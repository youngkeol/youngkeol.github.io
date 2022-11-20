---
layout: default
title: 프로미스
grand_parent: 자바스크립트
parent: 자바스크립트 기초
has_children: false
permalink: /docs/javascript/promise
nav_order: 10
---


### **프로미스란**
자바스크립트에서 비동기처리를 하기 위한 방법

>#### **동기 처리(Synchronous)란**
> 요청과 그결과가 동시에 일어난다는 뜻으로 순서가 정해져 있음
> ex) A작업 처리 시, A작업이 완료될 때까지 B작업은 대기

>#### **비동기 처리(ASynchronous)란**
> 요청과 결과가 동시에 일어나지 않는단는 뜻으로 응답을 기다리지 않고 새로운 요청을 보냄
> ex) A작업 처리 시, B작업도 처리



```js
let promise = new Promise(function(resolve, reject) {
    //resolve(value)  정상적인 경우
    //reject(error)  에러가 발생한 경우
});

promise.then(
  function(result) { /* 결과(result) */ },
  function(error) { /* 에러(error) */ }
)
.catch(
    //에러가 발생한 경우
);

```

### **참고**
> [poiemaweb - 동기식 처리 모델 vs 비동기식 처리 모델](https://poiemaweb.com/js-async){:target="_blank"}  
> [poiemaweb - 프로미스](https://poiemaweb.com/es6-promise){:target="_blank"}  
> [w3schools - 프로미스](https://www.w3schools.com/js/js_promise.asp){:target="_blank"}  