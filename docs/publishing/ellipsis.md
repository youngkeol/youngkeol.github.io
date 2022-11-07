---
layout: default
title: 말줄임표 만들기
parent: 웹퍼블리싱
permalink: /docs/web-publishing/ellipsis
nav_order: 1
---

## **말줄임표 만들기**

게시판의 제목이 길어질 경우 '...'으로 처리하는 방법


### **말줄임표(1줄)**
{% highlight html linenos %}
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<title>말줄임표만들기</title>
	<style>
		body {padding:100px;}
		a {color: #000; text-decoration: none; outline: none}
 		a:hover, a:active {text-decoration: none; color:#000; background-color:#fff;}

		.txt1 { display:block; width:200px; border:1px solid black; padding:0 30px 0 10px; box-sizing:border-box;
			/*줄바꿈처리 : 한줄처리(줄바꿈x)*/
			white-space: nowrap;
			/*튀어나온 것을 없앤다*/
			overflow:hidden;
			/*글자가 넘을 경우 ...만들기*/
			text-overflow:ellipsis;
		}

		.txt2 {  display:block; width:200px; border:1px solid black;  padding:0 30px 0 10px;
            box-sizing:border-box; margin-top:100px;
			white-space:normal; overflow:hidden; text-overflow:ellipsis;
			display:-webkit-box; -webkit-line-clamp:2; -webkit-box-orient:vertical;
		}
	</style>
</head>
<body>	
	<h2>말줄임표 만들기(···)</h2>
	<a href="#" class="txt1">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</a>
	<a href="#" class="txt2">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</a>
</body>
</html>

{% endhighlight %}

### **말줄임표(2줄)**
{% highlight css linenos %}
txt2 {  
    display:block;
    width:200px; 
    border:1px solid black;
    padding:0 30px 0 10px;
    box-sizing:border-box; margin-top:100px;
    white-space:normal; overflow:hidden; text-overflow:ellipsis;
    display:-webkit-box; -webkit-line-clamp:2; -webkit-box-orient:vertical;
}
{% endhighlight %}


### **표식이 있는 말줄임표**



### ***예제 파일 다운로드**

<a href="./20221103.html" download>말줄임표 예제</a>