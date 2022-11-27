---
layout: default
title: 스코프 & 호이스팅
grand_parent: 자바스크립트
parent: 자바스크립트 기초
has_children: false
permalink: /docs/javascript/scope
nav_order: 1
---


### **스코프**
스코프란 유효범위/접근 가능한 범위로 전역 스코프와 지역 스코프가 있음

>#### **전역 스코프(Global scope)**
> 전역에 선언되어 코드 어디서든 참조 가능  
> ex) window 객체


>#### **지역 스코프(Local scope)**
> 함수 코드 블록이 만들 스코프로 자신과 하위 함수에서만 참조 가능  
>
>>##### **함수 레벨 스코프(Function-level scope)**
>> 함수 레벨 스코프란 함수 내의 스코프가 형성된것을 의미함  
>> 자바스크립트는 함수 레벨 스코프를 따름  
>> 함수 내에서 선언된 매개변수와 변수는 함수 외부에서는 유효하지 않음  
>> ex) var
>>
>>```js
>>var a = 10;
>>(function () {
>>  var b = 20;
>>})();
>>
>>console.log(a); // 10
>>console.log(b); // "b" is not defined
>>```
>>
>>##### **블록 레벨 스코프(Block-level scope)**
>> 블록 레벨 스코프란 블록 내의 스코프가 형성되는 것을 의미함
>> 자바스크립트는 함수 레벨 스코프를 따르지만, let, const의 등장으로 블록 레벨 스코프도 가능함
>> ex) 함수 코드 블록? if, for, while, try/catch 등
>>
>>```
>>if (true) {
>>  var x = 5;
>>}
>>console.log(x); // 5
>>```





### **호이스팅**
호이스팅이란 코드 실행전 변수/함수의 선언/초기화하고, 해당 스코프 최상단에 끌어 올려주는것
>
>```js
>console.log(test); //undefined (선언 + 최기화 : 호이스팅)
>var test = 'test'; // (선언 + 초기화 + 할당)
>console.log(test); //test
>```

### **전역 스코프**
> [poiemaweb - 스코프](https://poiemaweb.com/js-scope)


