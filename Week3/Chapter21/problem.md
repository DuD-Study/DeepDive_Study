# Chapter 21

<pre>1. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```js
console.log(x); // 1. ?
console.log(y); // 2. ?

var x = 1;

function foo() {
  y = 2;
}
foo();

console.log(x + y); // 3. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. undefined<br>2. ReferenceError<br>3. 3</strong>
  <pre>1. var키워드로 선언한 x변수는 호이스팅이 발생하여 undefined를 반환한다.<br>2. y는 변수 선언 없이 전역 객체의 프로퍼티로 추가 했기 때문에 호이스팅이 발생하지 않아 ReferenceError가 발생한다.</pre>
</details>

<br>

<pre>2. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```js
parseFloat('3.14');
parseFloat('34 22 46');
parseFloat('30 years');
```

<details>
  <summary>Solution</summary>
  <strong>3.14 <br>34</br> 30  </strong>
  <pre>parseFloat는 전달받은 문자열 인수를 실수로 해석하여 반환하는데 공백으로 구분된 문자열은 첫 번째 문자열만 반환한다.</pre>
</details>

<br>

<pre>3. 다음 코드의 실행결과를 예측하시오.</pre>

```js
const obj = eval("{a: 1}");
const func = eval("function() {return 2}");
const multi = eval("1 + 2; 3 + 4;");

console.log(obj, func, multi);
```

<details>
<summary>Solution</summary>
<Strong>1, SyntaxError, 7</Strong>
<pre>객체와 함수리터럴은 반드시 괄호로 둘러싸야 정상동작하며, 인수가 여러 개의 문이면 마지막 결과 값을 반환한다.</pre>
</details>

<br>

<pre>4. 빈칸을 채워 넣어 보시오</pre>

<pre>1. 기존에 전역 객체는 브라우저 환경(window)과 Node.js 환경(global)에서 식별자를 달리 사용했는데, 
        둘을 통일 한 식별자 [ 1.         ]가 ES11에서 도입되었다. 

2. 밑에 코드처럼 원시값이 마치 객체처럼 동작하는 이유는 자바스크립트 엔진이 암묵적으로 연관된 객체를 생성하여 그 객체로 
   프로퍼티에 접근하거나 메소드를 호출하고 다시 원시 값을 되돌리기 때문인데, 그 임시 객체를 [ 2.         ]라고 한다. 
</pre>

```js
const str = 'deepdive';

console.log(str.length)   // 8
console.log(str.toUpperCase()) // DEEPDIVE
```
<pre>3. 방금 위에서 [2.          ]는 식별자에 원시값을 되돌리고 [ 3.              ]의 대상이 되어버림. </pre>


<details>
  <summary>Solution</summary>
  <strong>1.globalThis (p.326) <br>2.래퍼 객체(p.323) </br>3. 가비지 컬렉션 (p.324) </strong>
</details>

<br>