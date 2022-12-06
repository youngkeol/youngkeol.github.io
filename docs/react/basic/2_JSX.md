---
layout: default
title: 2_JSX란
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/jsx
nav_order: 2
---

### **JSX란?**   

Javascript의 확장 문법으로 JSX를 사용하면, React에서 HTML을 쉽게 작성 가능.


### **JSX 표현식**  

JSX를 사용하면 ```{}``` 안에 표현식 사용 가능
    표현식은 React변수, 속성, JavaScript 표현식  
```jsx
const myElement = <h1>React is {5 + 5} times better with JSX</h1>;
```  

### **JSX 규칙**  
1. HTML코드는 하나의 최상위 요소가 감싸는 형태
```jsx
function Element(){
	return (
		<div>
            <p>I am a paragraph.</p>
            <p>I am a paragraph too.</p>
        </div>
	);
}
```  


2. JSX는 XML규칙을 따르므로 HTML 요소를 제대로 닫아야 함
```jsx
function Element(){
	return (
		<input type="text" />;
	);
}
```


3. class 대신 className 사용
```jsx
function Element(){
	return (
		<div className="tit">React</div>
	);
}
```


4. React는 if명령문을 지원하지만, JSX 내부에서는 지원하지 않음  
(JSX에서 조건문을 사용할려면, JSX외부에 명령문을 넣거나, 삼항 표현식으로 사용 가능)
```jsx
function Element(){
	let falg = true;
    let text = "";
    if(flag) { 
        text = "HI";
    } else { 
         text = "BYE"; 
    }
    return (
		<div>{text}</div>
	);
}
```
```jsx
function Element(){
	let falg = true;
    return (
		<div>{falg == true? HI : BYE}</div>
	);
}
```



### **참고**

> [리액트 홈페이지 - JSX 소개](https://reactjs-kr.firebaseapp.com/docs/introducing-jsx.html){:target="_blank"}  
> [w3schools 리액트 튜토리얼 - JSX](https://www.w3schools.com/REACT/react_jsx.asp){:target="_blank"}
