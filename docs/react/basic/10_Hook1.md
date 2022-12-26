---
layout: default
title: 10_Hook1
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/hook1
nav_order: 10
---


### **Hook**  
함수형 컴포넌트에서 상태 관리, 렌더링 직후 작업 등을 할 수 있게 해주는 기능

> Hook 사용 규칙
> 1. 무조건 최상위 레벨에서만 호출
> 2. 컴포넌트가 렌더링 될때 매번 같은 순서로 호출
> 3. 리엑트 함수 컴포넌트에서만 Hook 호출

### **useState**  
데이터가 사용자 인터페이스에 반영되어야 한다면  state를 사용함  
일반적인 변수와 달리 state를 사용하여 값을 설정하고, state가 바뀌면 재렌더링 되어 화면에 반영됨  

useState를 사용해서 상태를 등록하면 항상 두개의 변수를 반환함
(첫번째는 현재의 상태값, 두번째는 업데이트하는 함수)

>const 변수를 사용하는 이유
>등호(=)을 통해 값을 할당하지 않고, 함수를 통해 값을 바꾸는데
>이 값은 리엑트에서 관리되기 때문에 상수형 사용가능



```jsx
import { useState } from "react";

const Plus = (props) => {
    const [number, setNumber] = useState(1); //useState사용(값이 변경될때마다 해당 컴포넌트 재렌더링)

    const clickhandler = () => {
        let newNum = number+1;
        setNumber(newNum);
    }

    return (
        <div>
            <div>{number}</div>
            <button onClick={clickhandler}>plus</button>
        </div>
    )
}
```


### **useEffect**  
컴포넌트가 렌더링 될때 특정 작업을 수행할 수 있도록 하는 Hook.

> 형식
> import React, {useEffect} from 'react';  
> useEffect (()=> {   
>   return ()=>{};  
> }, [dependency])  
> function : 수행하고자 하는 작업  
> dependency : 배열의 형태로 검사하고자 하는 특정값 (빈배열일 경우 : 화면에 가장 처음 렌더링 될때 한번만 실행 )

> Side Effect란?  
> 컴포넌트가 화면에 렌더링된 이후 비동기로 처리되어야 하는 부수적인 효과  
> 외부에서 호출하는 API ```useEffect(<function>, <dependency>)```  

```jsx
//생량한 경우 : 렌더링 될때마다 실행
import { useEffect } from "react";
const Example = ()=>{
    useEffect(()=>{
        console.log("렌더링 될때 마다 실행");
    })
}
```
```jsx
//빈배열인 경우 : 처음 한번만 실행
import { useEffect } from "react";
const Example = ()=>{
    useEffect(()=>{
        console.log("처음 한번만 실행");
    },[])
}
```

```jsx
//값이 있는 경우 : 특정 props, state가 변경될 경우 실행
import { useEffect } from "react";
const Example = ()=>{
    useEffect(()=>{
        console.log("name 값이 변경된 경우 실행");
    },[name]);
}
```




### **useMemo**

### **useCallback**

### **useCallRef**



### **참고**
> [w3schools 리액트 튜토리얼 - hook](https://www.w3schools.com/REACT/react_hooks.asp){:target="_blank"}
> [리액트 홈페이지 - hook](https://ko.reactjs.org/docs/hooks-intro.html){:target="_blank"}
