---
layout: default
title: 6_List&key
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/list-key
nav_order: 6
---


### **List & Key**
- key는 React에서 어떤 항목을 변경, 추가, 삭제할지 식별을 도움  
- key는 고유한 값이어야하고, 변하지 않는 값을 할당해함  
- 고유한 값이 없다면 차선책으로 리스트의 위치 index를 사용할 수 있지만 좋은 방법은 아님(리스트가 추가 삭제될 경우 순서가 변경될 수 있기 때문임)  
- key는 props.key 로 읽어오는 것이 안됨  


```jsx
function NumberList = (props) =>{
    const numbers = [1, 2, 3, 4, 5];
    const listItem = numbers.map((number, index)=>{
        <li key={number.toString()}>
        {number}
        </li>
    });

    return (
        <ul>
            {listItem}
        </ul>
    )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<NumberList/>);
```



### **참고**
> [리액트 홈페이지 - list & key](https://ko.reactjs.org/docs/lists-and-keys.html){:target="_blank"}
