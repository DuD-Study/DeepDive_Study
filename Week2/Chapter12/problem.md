# Chapter 12

<pre>1. 함수 내부로 입력을 전달받는 변수를 [       ], 입력을 [        ], 출력을 [           ]이라한다. </pre>

<details>
  <summary>Solution</summary>
    <strong>변수(Parameter), 인수(argument), 반환값(return value)</strong>
</details>

<br>

<pre>2. 함수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징을 함수 [       ]이라 한다. 
</pre>

<details>
  <summary>Solution</summary>
  <pre>호이스팅</pre>
</details>

<br>

<pre>3. 아래의 코드를 보고 실행 결과를 예측하시오.
</pre>

```js
(function foo() {
  console.log("hi");
});
foo(); // 1. ?
{
  function bar() {
    console.log("hello");
  }
}
bar(); // 2. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. ReferenceError: foo is not defined<br>2. hello</strong>
  <pre>그룹 연산자 () 내에 있는 함수 리터럴(foo)은 함수 선언문으로 해석되지 않고 함수 리터럴 표현식으로 해석된다. 그룹 연산자의 피연산자는 값으로 평가될 수 있는 표현식이어야 하기 때문에 함수선언문인 foo는 피연산자로 사용할 수 없다.</pre>
</details>

<br>

<pre>4. 함수의 매개변수를 통해 다른 함수의 내부로 전달되는 함수를 [       ],<br> 매개변수를 통해 함수의 외부에서 콜백함수를 전달받은 함수를 [       ]라 한다. </pre>

<details>
  <summary>Solution</summary>
    <strong>콜백함수, 고차함수</strong>
</details>

<br>
