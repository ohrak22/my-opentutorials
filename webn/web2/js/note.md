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

### 비교 연산자와 Boolean 데이터 타입
ex4.html
~~~
<script>
     document.write(1===1);
</script>
~~~

### 조건문
ex5.html
~~~
<script>
	document.write("1<br>");
	if (true) {
		document.write("2<br>");
	} else {
		document.write("3<br>");
	}
	document.write("4<br>");
</script>
~~~

### 조건문의 활용
night_day 버튼을 만들고 조건에 따라 색을 바꾸는 코드를 만든다.

3.html
~~~
<input id="night_day" type="button" value="night" onclick="
    if(document.querySelector('#night_day').value === 'night'){
      document.querySelector('body').style.backgroundColor = 'black';
      document.querySelector('body').style.color = 'white';
      document.querySelector('#night_day').value = 'day';
    } else {
      document.querySelector('body').style.backgroundColor = 'white';
      document.querySelector('body').style.color = 'black';
      document.querySelector('#night_day').value = 'night';
    }
  ">
~~~

### 리팩토링(refactoring)
this와 var를 이용해 코드를 더 간결하게 만들기
~~~
<input id="night_day" type="button" value="night" onclick="
   var target = document.querySelector('body');
   if(this.value === 'night'){
     target.style.backgroundColor = 'black';
     target.style.color = 'white';
     this.value = 'day';
   } else {
     target.style.backgroundColor = 'white';
     target.style.color = 'black';
     this.value = 'night';
   }
">
~~~

### 배열
ex6.html

### 반복문
ex7.html

### 배열과 반복문
ex8.html

### 함수
ex9.html
Basic  
Parameter & Argument  
Return

### 함수 활용
nightDayHandler 함수를 만들고 night_day onclick 이벤트에서 호출한다.
~~~ html
<input id="night_day" type="button" value="night" onclick="nightDayHandler(this);">
~~~
~~~ js
function nightDayHandler(self) {
	var target = document.querySelector('body');
	if (self.value === 'night') {
		Body.setBackgroundColor('black');
		Body.setColor('white');
		self.value = 'day';

		Links.setColor('white');
	} else {
		Body.setBackgroundColor('white');
		Body.setColor('black');
		self.value = 'night';

		Links.setColor('blue');
	}
}
~~~

### 객체
객체를 만들고 사용하기  
10.html  
Create
~~~
var coworkers = {
	"programmer": "egoing",
	"designer": "leezche"
};
document.write("programmer : " + coworkers.programmer + "<br>");
~~~
Iterate
~~~
for (var key in coworkers) {
	document.write(key + ' : ' + coworkers[key] + '<br>');
}
~~~
Property & Method
~~~
coworkers.showAll = function () {
	for (var key in this) {
		document.write(key + ' : ' + this[key] + '<br>');
	}
}
coworkers.showAll();
~~~

### 객체 활용
Body 객체를 만들고 setColor와 setBackgroundColor 함수를 넣는다.
~~~ js
var Body = {
	setColor: function (color) {
		//document.querySelector('body').style.color = color;
		$('body').css('color', color);
	},
	setBackgroundColor: function (color) {
		// document.querySelector('body').style.backgroundColor = color;
		$('body').css('backgroundColor', color);
	}
}
~~~
Links 객체를 만들고 nightDayHandler 함수를 수정한다.

### 파일로 쪼개서 정리 정돈하기
colors.js 파일을 만들고 스크립트 코드를 옮긴다.  
모든 파일의 head 태그에 다음 코드를 넣어준다.
~~~
<script src="colors.js"></script>
~~~

### 라이브러리와 프래임워크
CDN을 통해 jquery를 사용한다.  
head에 다음 코드를 작성한다.
~~~
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
~~~
colors.js
~~~
$('a').css('color', color);
~~~

### UI vs API
User Interface
Application Programming Interface

### 수업을 마치며


