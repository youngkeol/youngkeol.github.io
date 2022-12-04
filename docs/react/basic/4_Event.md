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




### **참고**
> [w3schools 리액트 튜토리얼 - react_components](https://www.w3schools.com/REACT/react_components.asp){:target="_blank"}

