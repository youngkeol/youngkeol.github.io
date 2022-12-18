---
layout: default
title: 7_Forms
grand_parent: 리액트
parent: 리액트 기초
has_children: false
permalink: /docs/react/basic/forms
nav_order: 7
---


### **Forms**
React에서는 일반적으로 사용자의 입역을 기반으로 state를 관리하고 업데이트 함  


```jsx
import { useState } from "react";

const JoinForm = (props) => {
    const [name, setName] = useState('');
    const [birthYear, setBirthYear] = useState('');
    const [introduction, setIntroduction] = useState('');

    //전송이벤트
    const submitHandler = (e)=>{
        e.preventDefault();
    }

    //textarea 변경 이벤트
    const introductionHandler = (e) => {
        setIntroduction(e.target.value);
    }

    return (
        <div>
            <form onSubmit={submitHandler}>
                <label htmlFor="name">Name
                    <input id="name" type="text" name="name" 
                        defaultValue={name} 
                        onChange={(e)=> setName(e.target.value)}
                    />
                </label>
                <label htmlFor="birth_year">BirthYear
                    <select id="birth_year" name='birthYear' 
                        defaultValue={birthYear} 
                        onChange={(e)=> setBirthYear(e.target.value)}
                    >
                        <option value="1994">1994</option>
                        <option value="1995">1995</option>
                    </select>
                </label>
                <label htmlFor="introduction">Introduction
                    <textarea id="introduction" name="introduction" cols="30" rows="10" 
                        defaultValue={introduction}  
                        onChange={introductionHandler} 
                    />
                </label>
                <button>join</button>
            </form>
        </div>
    )
}
export default JoinForm;
```


### **참고**
> [리액트 홈페이지 - forms](https://ko.reactjs.org/docs/forms.html){:target="_blank"}  
> [w3schools 리액트 튜토리얼 - forms](https://www.w3schools.com/REACT/react_forms.asp){:target="_blank"}  


