---
layout: default
title: 9_Style
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/style
nav_order: 9
---


### **인라인 스타일**
카멜 케이스(camelCase) 방식으로 작성해야 함

```jsx
//방법1
const InlineStyle = (props) => {
    return <div style={{color:'#fff', backgroundColor:'rgb(255 136 136)'}}>inline-style</div>
}
```

```jsx
// 방법2
const InlineStyle = (props) => {
    const style = {
        color:'#fff',
        backgroundColor: 'rgb(255 136 136)'
    }
    return  <div style={style}>자바스립트 객체 + inline-style</div>
}
```


### **CSS 스타일시트**
별도의 CSS 스타일을 호출 (import 사용)
```jsx
import './style.css';
```

### **CSS 모듈**
CSS 모듈을 사용하여 추가하는 방법으로 이름 충돌에 걱정할 필요가 없음  
```.module.css``` 형식으로 사용

```jsx
import styles from './style.moudule.css';
const InlineStyle = (props) => {
    return <div className={styles.tit}>CSS 모듈</div>
}
```

  
    


> CSS-in-JS 방식
> styled-components, emotion
> Javascript 파일 내에서 CSS를 사용할수 있게 해주는 CSS-in-JS 라이브러리



### **참고**
> [w3schools 리액트 튜토리얼 - css](https://www.w3schools.com/REACT/react_css_styling.asp){:target="_blank"}