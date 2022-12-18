---
layout: default
title: 3_Components&Props
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/components-props
nav_order: 3
---



### **Components**  
컴포넌트는 독립적이고 재사용 가능한 코드 조각으로 HTML을 반환함

```jsx
//함수형 컴포넌트
function Car () {
    return (
        <div>
            <h2>Car</h2>
        </div>
    )
}
```





### **Props**
부모 컴포넌트에서 자식 컴포넌트로 속성을 전달달함

```jsx
//함수형 컴포넌트
function Car (props) {
    return (
        <div>
            <h2>Car</h2>
            <h3>color : {props.color}</h3>
        </div>
    )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car color="red"/>);
```


### **참고**
> [w3schools 리액트 튜토리얼 - react_components](https://www.w3schools.com/REACT/react_components.asp){:target="_blank"}

