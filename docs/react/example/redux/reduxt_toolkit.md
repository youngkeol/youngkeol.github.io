---
layout: default
title: redux toolkit란?
grand_parent: 리액트
parent: 리액트 예제
has_children: false
permalink: /docs/react/example/redux_toolkit
nav_order: 1
---


### **redux toolkit란?** 



### **redux toolkit 설치** 
```shell
//만약 redux가 설치되어 있으면 삭제해야함(이미 redux toolkit에 포함되어 있음)
npm install @reduxjs/toolkit
```


### **redux toolkit 사용 방법**

```js
//src/store/index.js
//리덕스 스토어 생성
import { configureStore } from '@reduxjs/toolkit';
import counterReducer from './counter';

const store = configureStore({
    reducer: {
        counter: counterReducer,
    }
});

export default store;
```

```js
//src/store/counter.js
import { createSlice } from '@reduxjs/toolkit';
const initalCounterStore = {
    counter: 0
}
const counterSlice = createSlice({
    name: 'counter', //이름
    initialState: initalCounterStore, //초기값
    reducers: { //메서드
        increment(state, action) {
            state.counter = state.counter + action.payload;
        },
        decrement(state, action) {
            state.counter = state.counter - action.payload;
        },
    }
})
```

```js
//컵포넌트에서 사용
import { useSelector, useDispatch } from 'react-redux';
import { counterActions } from '../store/counter';
const Counter = () => {
  const dispatch = useDispatch(); // reduce에 대한 엑션을 보냄
  const counter = useSelector(state => state.counter.counter);

  const incrementHandler = (e, params) => {
    dispatch(counterActions.increment(params));
  };

  const decrementHandler = (e, params) => {
    dispatch(counterActions.decrement(params));
  };

  return (
    <main>
      {counter}
      <div>
        <button onClick={(e) => { incrementHandler(e, 1) }}>Increment</button>
        <button onClick={(e) => { decrementHandler(e, 1) }}>Decrement</button>
      </div>
    </main >
  );
};

export default Counter;
```



### **참고**
> [redux toolkit](https://redux-toolkit.js.org/introduction/getting-started){:target="_blank"}