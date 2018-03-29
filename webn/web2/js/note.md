### HTML과 JavaScript의 만남 1
script 태그를 사용해 JavaScript를 실행한다.  
ex1.html
~~~
<script>
	document.write(1+1);
</script>
~~~
html은 정적이지만 자바스크립트는 동적이다.

### HTML과 JavaScript의 만남 2
input 태그를 만들기.  
ex2.html
~~~
<input type="button" value="hi" onclick="alert('hi')">
~~~
### HTML과 JavaScript의 만남 3
콘솔에서 자바 스크립트 바로 실행하기.  
브라우저에서 F12를 누른후 후 콘솔 탭에서 스크립트 코드 실행.
~~~
alert('hi')
~~~
### 데이터타입 - 문자열과 숫자
브라우저 콘솔에서 문자열 코드 실행.
~~~
1+1
2
"Hello world"
"Hello world".length
11
"Hello world".toUpperCase()
"HELLO WORLD"
"Hello world".indexOf('o')
4
~~~

### 변수와 대입 연산자
변수와 대입 연산자 설명.

### CSS 기초
ex3.html

### 제어할 태그 선택하기
body 태그를 선택하고 style 속성을 변경하기.
~~~
document.querySelector('body').style.backgroundColor = 'black';
~~~
night와 day 버튼을 만들고 클릭하면 backgroundColor와 text color를 바꾸는 코드를 만든다.
3.html
~~~
<input type="button" value="night" onclick="
    document.querySelector('body').style.backgroundColor = 'black';
    document.querySelector('body').style.color = 'white';
">
<input type="button" value="day" onclick="
    document.querySelector('body').style.backgroundColor = 'white';
    document.querySelector('body').style.color = 'black';
">
~~~
