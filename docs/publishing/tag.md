---
layout: default
title: 블록 & 인라인
parent: 웹퍼블리싱
permalink: /docs/web-publishing/tag
nav_order: 2
---

### **블록 태그(block)** 
블록 태그는 전체 공간을 차지해서 언제나 새로운 라인에서 시작

1. 수직으로 쌓임
2. width/height 적용 가능 (default:with:100%; height:내부 컨텐츠 만큼) 
3. margin / padding 적용 가능

```html
<div>, <h1>, <p>, <li>, <form>
```

{: .warning-title  }
> ※주의  
> p태그 아에 블록 요소를 포함 불가 (블록 요소 넣을 시 웹표준 어긋남)



### **인라인 태그(inline)** 
인라인 태그는 콘텐츠의 흐름을 끊지 않고, 요소를 구성하는 태그에 할당된 공간만 차지  

1.  수평으로 쌓임  
2. width/height 적용 불가 (default:내부 컨텐츠 만큼)
3. margin / padding 좌우만 적용 가능

```html
<span>, <a>, <em>, <i>, <strong>
```
  
{: .warning-title  }
> ※주의      
> 인라인 요소는 블록 요소 포함 불가 (블록 요소 넣을 시 웹표준 어긋남)  
> HTML5에 한해서 a태그 안에 블록 요소 포함 가능


### **인라인 블록 태그(inline-block)** 
인라인 블록 태그는 인란인 태그의 특징과 블록 태그의 특징을 모두 가짐
1. 수평으로 쌓임
2. width/height 적용 가능 (default:내부 컨텐츠 만큼)

```html
<button>, <input>, <select>, <textarea>, <img>
```


### **시멘틱 태그** 
의미가 있는 태그로 HTML5로 만드는 웹 문서의 내용이 태그만 보고도 알수 있도록 등장  
검색엔진최적화/ 소스코드 구조화 / 코드 가독성 향상 등의 특징을 가짐


```html
<header>, <nav>, <section>, <aside>, <article>, <footer>
```





