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


