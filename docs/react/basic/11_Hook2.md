---
layout: default
title: 11_Hook2
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/hook2
nav_order: 11
---



### **Context**
React Context는 전역적으로 상태를 관리하는 방법으로 중접된 컴포넌트 간 상태를 쉽게 공유할 수 있음  


> Context란
> 일반적으로 데이터를 전달할 떄 props를 통해 전달되지만, 여러 컴포넌트에게 전달해야할 경우 전역으로 > > > > context를  사용하여 전달 함
> createContext : context객체 생성
> Provider : 생성한 context객체를 하위 컴포넌트한테 전달하는 역할
    

```jsx
import { useState, createContext, useContext } from "react";
import ReactDOM from "react-dom/client";

const UserContext = createContext();

function Component1() {
    const [user, setUser] = useState("Hong gil dong");

    return (
        <UserContext.Provider value={user}>
            <Conponet2 />
        </UserContext.Provider>
    )
}

function Component2() {
    return (
        <Component3 />
    )
}

function Component3() {
    const user = useContext(UserContext);

    return (
        <div>{user}</div>
    )
}
```

### **useRef**
리렌더링 하지 않고 특정 DOM을 선택하여 컨트롤 하는 Hook


1. 특정 DOM 선택
2. 컴포넌트 안의 변수 생성
3. 리렌더링 방지

>
>
>

```jsx
//포커스 구현
import { useState, useRef } from "react";

const Example = () => {
    const [text, setText] = useState('');
    const inputRef = useRef();

    const changeHandler = (e) => {
        setText(e.target.value);
    }
    const resetHandler = (e) => {
        e.preventDefault();
        setText('');
        inputRef.current.focus();
    }
    return (
        <div>
            <input 
                ref = {inputRef}
                value = {text}
                onChange = {changeHandler}
            />
            <button onClick = {resetHandler}>Reset</button>
        </div>
    )

} 
```