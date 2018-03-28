### CSS 등장 이전의 상황
font 태그를 이용해 color를 바꾼다.
~~~
<font color="red">WEB</font>
~~~

### CSS의 등장
디자인 부분을 처리하기 위한 기술.
~~~
<style>
	a {
		color: black;
	}
</style>
~~~


### 혁명적 변화
#### 속성
태그에 style 속성을 사용해 본다.
~~~
<a href="2.html" style="color:red;text-decoration:underline">CSS</a>
~~~
여러개의 속성 사용시 세미콜론으로 구분.
#### 혁명적 변화
* a는 선택자(Selector)
* color: black; 부분은 선언(Declaration)
* color는 속성(Property)
* black는 값(Value)

### CSS 속성을 스스로 알아내는 방법
css text size property 검색
css text center property
~~~
font-size: 45px;
text-align: center;
~~~

### CSS 선택자를 스스로 알아내는 방법
태그에 class 속성을 추가한다.
~~~
<a href="2.html" class="saw" id="active">CSS</a>
~~~
선택자 앞에 .을 추가하여 class를 선택한다.
~~~
.saw {
	color: gray;
}
~~~
선택자 앞에 #이 오면 id가 선택된다.
~~~
#active {
	color: red;
}
~~~
##### 선택자 우선순위
아이디 > 클래스 > 태그
포괄적인 것이 우선 순위가 낮다. 포괄적인 것 부터 작업하고 세부적인 것을 나중에 작업하기 위함이다.

##### 그 밖에 선택자
css selector 검색

### 박스모델
black level element
inline element
css box model 검색

##### 박스모델 사용
~~~
h1 {
	font-size: 45px;
	text-align: center;
	border-bottom: 1px solid gray;
	margin: 0;
	padding: 20px;
}
ol {
	border-right: 1px solid gray;
	width: 100px;
	margin: 0;
	padding: 20px;
}
~~~

### 그리드
아무의미 없는 디자인용 태그
div: block level
span: inline level

div 태그에 grid 아이디 추가
~~~
<div id="grid">
	<div>NAVIGATION</div>
	<div>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
	<div>test.</div>
</div>
~~~
스타일 추가
~~~
<style>
	#grid {
		border: 5px solid pink;
		display: grid;
		grid-template-columns: 150px 2fr 1fr;
	}

	div {
		border: 5px solid gray;
	}
</style>
~~~
그리드 아이디 하위 태그 선택
~~~
#grid ol {
	padding-left: 33px;
}
~~~

## 반응형 디자인과 미디어 쿼리 소개
화면의 크기에 따라 디자인이 바뀌는 페이지 만들기  
style.css  
~~~
@media(max-width:800px) {
    #grid {
        display: block;
    }

    ol {
        border-right: none;
    }

    h1 {
        border-bottom: none;
    }
}
~~~




