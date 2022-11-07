---
layout: default
title: 말줄임표 만들기
parent: 웹퍼블리싱
permalink: /docs/web-publishing/ellipsis
nav_order: 1
---

## **말줄임표 만들기**

게시판의 제목이 길어질 경우 '...' 으로 처리하는 방법


### **말줄임표(1줄)**

```css
.txt1 { display:block; width:200px; 
 	padding:0 30px 0 10px; 
 	box-sizing:border-box;
	white-space: nowrap; /*줄바꿈처리 : 한줄처리(줄바꿈x)*/
	overflow:hidden; /*튀어나온 것을 없앤다*/
	text-overflow:ellipsis; /*글자가 넘을 경우 ...만들기*/
}
```

### **말줄임표(2줄)**

```css
txt2 {  
    display:block;
    width:200px; 
    padding:0 30px 0 10px;
    box-sizing:border-box; margin-top:100px;
    white-space:normal; overflow:hidden; text-overflow:ellipsis;
    display:-webkit-box; -webkit-line-clamp:2; -webkit-box-orient:vertical;
}
```


### **뒤에 날짜가 있는 말줄임표**
```css
.list-box {list-style:none; width:100%;}
.list {display:inline-block; overflow: hidden; max-width: 100%; white-space: nowrap;}
.list .title {display:block; float:left; overflow: hidden; width:calc(100% - 100px); text-overflow: ellipsis; white-space: nowrap;}
.list .date {display:block; float:left; width:100px; text-align:center; }
```

```html
<ul class="list-box">
	<li>
		<div class="list">
			<span class="title"><a href="#">Lorem ipsum dolor sit amet, consectetur adipisicing elit</a></span>
			<sapn class="date">2022-11-07</sapn>
		</div>
	</li>
	<li>
		<div class="list">
			<span class="title"><a href="#">Lorem ipsum dolor sit amet, consectetur adipisicing elitLorem ipsum dolor sit amet</a></span>		
			<sapn class="date">2022-11-08</sapn>
		</div>
	</li>
</ul>
```

### **참고 이미지**

![alt 뒤에 날짜가 있는 말줄임표](./ellipsis_img_01.png)


### **예제 파일 다운로드**

[말줄임표](ellipsis_ex_01.html)  
[뒤에 날짜가 있는 말줄임표](ellipsis_ex_02.html)  
<a href="/docs/publishing/elipsis/ellipsis_ex_02.html" download>다운로드 테스트</a>