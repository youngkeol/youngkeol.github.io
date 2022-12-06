---
layout: default
title: 4_Event
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/event
nav_order: 4
---



### **Event**  
1. React의 이벤트는 카멜 케이스(camelCase) 사용
2. JSX를 사용하여 문자열이 아닌 함수로 이벤트 핸들러 전달



```jsx
const Test = (props) => {
    const clickhandler = () => {
        console.log('Clicked1');
    }

    return (
        <div>
            <button onClick={clickhandler}>이벤트 방법1</button>
            <button onClick={()=>{console.log('Clicked2')}}>이벤트 방법2</button>
        </div>
    )
}
```




### **참고**
> [리액트 홈페이지 - 이벤트 처리하기](https://www.w3schools.com/REACT/react_events.asp){:target="_blank"}
> [w3schools 리액트 튜토리얼 - react_event](https://ko.reactjs.org/docs/handling-events.html){:target="_blank"}
