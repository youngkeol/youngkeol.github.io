---
layout: default
title: 13_Hook4
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/hook4
nav_order: 13
---


### **useReducer**
복잡한 State 관리할 때 사용 (useState 비슷함)

> 형식
> import React, {useReducer} from 'react';
> const reducer= (state, action) =>{ ... }
> state : 컴포넌는 state
> action : type으로 분기하여 reducer state 상태 업데이트
>
> const [state, dispatch] = useReducer(reducer, initialState)
> state : 컴포넌는 state
> dispatch : reducer 함수 실행
> reducer : 외부에 정의한 reducer 함수
> initialState : 초기 state


```js
import React, { useReducer } from 'react';

const reducer = (state, action) => {
    if (action.type == 'plus') {
        return state + action.number;
    }
    if (action.type == 'minus') {
        return state - action.number;
    }

    if (action.type == 'mul') {
        return state * action.number;
    }
    if (action.type == 'div') {
        return state / action.number;
    }
}
const UseReducerTest = () => {
    const [number, dispatch] = useReducer(reducer, 0); //0 초기값

    return (
        <>
            <p>{number}</p>
            <button onClick={() => { dispatch({ type: "plus", number: 1 }) }}>+1</button>
            <button onClick={() => { dispatch({ type: "minus", number: 1 }) }}>-1</button>
            <button onClick={() => { dispatch({ type: "mul", number: 2 }) }}>*2</button>
            <button onClick={() => { dispatch({ type: "div", number: 2 }) }}>/2</button>
        </>
    );
};

export default UseReducerTest;
```


### **참고**
> [w3schools 리액트 튜토리얼 - react_useReducer](https://www.w3schools.com/REACT/react_usereducer.asp){:target="_blank"}