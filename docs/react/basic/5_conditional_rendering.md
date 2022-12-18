---
layout: default
title: 5_조건부 렌더링
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/conditional_rendering
nav_order: 5
---



### **조건부 렌더링1**  
특정 조건에 따라 렌더링 하는 것

```jsx
import React,{ useState } from "react";

const UserGreeting = (props) => {
    return  <div>Welcome</div>
};

const GuestGreeting = (props) => {
    return <div>Please sign up.</div>
};

function App() {
  const [isLoggedIn, setIsLoggedIn] = useState(false);

  if(isLoggedIn) {
    return <UserGreeting />
  }  else {
    return <GuestGreeting />
  }
}
```


### **조건부 렌더링2_인라인 (if-Else)** 
JSX 안에 중괄호를 이용하여 표현식 포함 가능 (condition ? true: false)
```jsx
function App() {
  const [isLoggedIn, setIsLoggedIn] = useState(false);

  return (
    <div>
      {isLoggedIn ?  <UserGreeting /> :  <GuestGreeting /> }
    </div>
  )
}
```


### **조건부 렌더링3_인라인 (논리 && 연산자)** 
JSX 안에 중괄호를 이용하여 표현식 포함 가능 (&& 사용)

```jsx
function App() {
  const [isLoggedIn, setIsLoggedIn] = useState(true);

  return (
    <div>
      {isLoggedIn &&  <UserGreeting /> }
      {!isLoggedIn &&  <GuestGreeting /> }
    </div>
  )
}
```






### **참고**
> [리액트 홈페이지 - 조건부 렌더링](https://ko.reactjs.org/docs/conditional-rendering.html){:target="_blank"}  
> [w3schools 리액트 튜토리얼 - 조건부 렌더링](https://www.w3schools.com/REACT/react_conditional_rendering.asp){:target="_blank"}
