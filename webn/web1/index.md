### 기획
![Image](https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3135/7547.png)


### HTML 코딩 실습 환경 준비
에디터(Editor) 설치


### 기본 문법 - 태그
1.html 파일을 만들고 다음 텍스트를 적어 넣는다.
~~~
Hypertext Markup Language (HTML) is the standard markup language for creating web pages and web applications.
~~~

##### 강조표시 
~~~
<strong>creating web pages</strong>

~~~

##### 밑줄
~~~
<u>web</u>
~~~

##### 헤더
~~~
<h1>This is heading 1</h1>
<h2>This is heading 2</h2>
<h3>This is heading 3</h3>
<h4>This is heading 4</h4>
<h5>This is heading 5</h5>
<h6>This is heading 6</h6>
~~~

##### 줄바꿈
~~~
<br>
~~~
br 태그는 닫지 않고 있다.
img, input, br, hr, meta 등은 닫지 않는 태그이다.
~~~
<p style="margin-top:45px;">
~~~
이것이 바로 CSS입니다
p 태그는 단락을 구분할 수 있어 더 의미있는 태그이다.

##### 이미지
~~~
<img src="https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3135/7648.png">
~~~
##### 부모 자식과 목록
~~~
<p>
    <a href="https://opentutorials.org">opentutorials</a>
</p>
~~~
##### 리스트
~~~
<ul>
  <li>1. HTML</li>
  <li>2. CSS</li>
  <li>3. JavaScript</li>
</ul>
<ul>
  <li>egoing</li>
  <li>k8805</li>
  <li>sorialgi</li>
</ul>
~~~


### 문서의 구조
본문은 body 태그로 본문을 설명하는 태그는 head 태그를 사용합니다.

##### head 태그
~~~
<title>WEB1 - html</title>
<meta charset="utf-8">
~~~
title 태그는 문서의 제목을 나타내며
meta charset="utf-8"은 이 문서가 utf-8 형식으로 작성된 문서라는 것을 나타냅니다.

##### body 태그
~~~
<body>
</body>
~~~

##### html 태그
~~~
<html>
</html>
~~~
head 태그와 body 태그를 감싸는 최상위 태그

##### 문서 타입
~~~
<!doctype html>
~~~
이 문서는 html 이라는 것을 명시합니다.

### 링크
~~~
<a href="https://www.w3.org/TR/html5/" target="_blank" title="html5 specification">Hypertext Markup Language (HTML)</a>
~~~