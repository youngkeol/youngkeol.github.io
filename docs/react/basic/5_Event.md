---
layout: default
title: 5_Event
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/components-props
nav_order: 5
---



### **Event**  

```js
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





### **Props**
부모 컴포넌트에서 자식 컴포넌트로 속성을 전달달함

```js
//함수형 컴포넌트
function Car (props) {
    return (
        <h2>{props.color}<h2>
    )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car color="red"/>);
```


### **참고**
> [w3schools 리액트 튜토리얼 - react_components](https://www.w3schools.com/REACT/react_components.asp){:target="_blank"}

