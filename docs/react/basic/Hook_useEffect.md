---
layout: default
title: Hook_useEffect
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/hook
nav_order: 11
---



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
> 외부에서 호출하는 API 
```react


```

### **useReducer**

> 형식
> import React, {useReducer} from 'react';
> const [satate, dispatchFn] = useReducer(reducerFn, initState, initFn)
>
> reducerFn : 리듀서 함수, 최신 state를 가져옴
> initState : 초기값
> initFn :  초기값 설정 함수



useSteate vs useRedycer
