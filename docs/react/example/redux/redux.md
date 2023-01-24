---
layout: default
title: redux란?
grand_parent: 리액트
parent: 리액트 예제
has_children: false
permalink: /docs/react/example/redux
nav_order: 1
---


### **redux란?**  
상태 관리 javascript 라이브러리  
Store라는 단일 전역 개체로 상태를 관리함(일관성 유지)



### **설치방법**
```shell 
npm install redux react-redux
```


### **사용방법**
보통 src/store에서 작업
```js
// src/store/index.js
//리덕스 스토어 생성
import { createStore } from 'redux';

const counterReducer = (state = { counter: 0 }, action) => {

    if (action.type === 'increment') {
        return {
            counter: state.counter + action.amount,
        }
    }

    if (action.type === 'decrement') {
        return {
            counter: state.counter - action.amount,
        }
    }

    return state;
}

const store = createStore(counterReducer);
export default store;
```

```js
//index.js
import React from 'react';
import ReactDOM from 'react-dom/client';
import { Provider } from 'react-redux'; //추가됨
import App from './App';
import store from './store/index'; //추가됨

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
    <Provider store={store}><App /></Provider>
);
```

```js
//컴포넌트에서 redux 사용
import classes from './Counter.module.css';
import { useSelector, useDispatch } from 'react-redux';

const Counter = () => {
  const dispatch = useDispatch(); // reduce에 대한 엑션을 보냄
  const counter = useSelector(state => state.counter);

  const incrementHandler = (e, params) => {
    dispatch({
      type: 'increment',
      amount:  params
    })
  };

  const decrementHandler = (e, params) => {
    dispatch({
      type: 'decrement',
      amount:  params
    })
  };

  return (
    <div>
      <div>COUNTER : {counter}</div>
      <div>
        <button onClick={(e) => { incrementHandler(e, 1) }}>Increment</button>
        <button onClick={(e) => { decrementHandler(e, 1) }}>Decrement</button>
      </div>
    </div>
  );
};

export default Counter;




```

>주의!
> 리듀서를 사용해서 반환할 때 기존 객체를 변경하면 에측하지 못하는 상황이 발생할 수 있음
> https://academind.com/tutorials/reference-vs-primitive-values

```
//잘못된 예
if (action.type === 'increment') {
    return {
        counter: state.counter++,
    }
}
```



### **참고**
> [redux](https://ko.redux.js.org/introduction/getting-started){:target="_blank"}
> [redux 튜토리얼](https://www.tutorialspoint.com/redux/index.htm){:target="_blank"}