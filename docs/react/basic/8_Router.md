---
layout: default
title: 8_Router(version 6)
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/router
nav_order: 8
---


### **React Router**
리엑트는 SPA 방식으로 새로운 페이지를 로드하는 방식이 아닌 URL에 따라 URL에 맞는 데이터를 렌더링 해주는 방식으로 React Router를 사용함  
(사용자가 요청한 URL에 따라 URL에 맞는 페이지를 보여주는 역할)



### **설치**
```
npm install react-router-dom
```



### **사용방법**

```jsx
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import Notice from '.co
function App() {
    return (
        <div>
            <BrowserRouter>
                <Route path="/" element= {<HomeWrapper />}></Route>
                <Route path="/Notice" element={< <Notice />}></Route>
                <Route path="*" element={<NotFound />} ></Route>   
            </BrowserRouter>
        </div>
    )
}
```