---
layout: default
title: 15_Fregment & Portals
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/fregment
nav_order: 15
---


### **Fregment**
- JSX 는 규칙상 하나의 태그로 묶어서 반환해야하는 규칙이 있어서, 불필요한 ```<div>```로 감싸는 것을 막고, 레이아웃을 유지하기 위해 사용

방법1(Fregments미사용)
```jsx
const Test = (props) => {
    return(
        <Fregments>
            <div>A</div>
            <div>B</div>
        </Fregments>
    )
}


```

방법2(Fregments미사용)
```jsx
const Wrapper = (props) => {
    return props.children
}
export default Wrapper;
```

```jsx
const Test = (props) => {
    return(
        <Wrapper>
            <div>A</div>
            <div>B</div>
        </Wrapper>
    )
}

```






### **Portals**
```html
    <div id="backdrop-root"></div>
    <div id="overlay-root"></div>
```
```JSX
import React, {Fragment} from 'react';
import ReactDOM from 'react-dom';

import Card from './Card';
import Button from './Button';
import classes from './ErrorMdal.module.css';

const Backdrop = (props) => {
    return <div className={classes.backdrop} onClick={props.onConfirm}> </div>
}

const ModalOverlay = (props) => {
    return (
        <Card className={classes.modal}>
            <header  className={classes.header}>
                <h2>{props.title}</h2>
            </header>
            <div className={classes.content}>
                <p>{props.message}</p>
            </div>
            <footer className={classes.actions}>
                <Button onClick={props.onConfirm} >Okay</Button>
            </footer>
        </Card>
    )
}
const ErrorModal = (props) => {
    return (
    <Fragment>
        {ReactDOM.createPortal(<Backdrop onClick={props.onConfirm}/>, document.getElementById('backdrop-root'))}

        {ReactDOM.createPortal(
            <ModalOverlay 
                title={props.title} 
                message={props.message} 
                onConfirm={props.onConfirm}
            />,
            document.getElementById('overlay-root')
        )}
    </Fragment>
    )
}

export default ErrorModal;
```

