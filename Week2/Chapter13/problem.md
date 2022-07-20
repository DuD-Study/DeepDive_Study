# Chapter 13

<pre>1. 아래 그림처럼 모든 스코프는 하나의 계층적 구조로 연결되며, 이런식으로 스코프가 계층적으로 연결된 것을 [            ]이라 한다.</pre>

<img src="https://velog.velcdn.com/images%2Fssu00%2Fpost%2Fe3e2c792-991e-41a8-9e09-7c8fa0173181%2F%EC%8A%A4%EC%BD%94%ED%94%8402.png" width=800px>

<details>
  <summary>Solution</summary>
    <strong>스코프 체인 ( Scope Chain )</strong>
</details>

<br>

<pre>2. 아래의 코드를 보고 실행 결과를 예측하시오.
</pre>

```js
var n1 = 1;
var n2 = "a";

function a() {
  var n1 = 2;
  b();
}

function b() {
  var n2 = "b";
  console.log(n1); // 1. ?
  c();
  function c() {
    console.log(n2); // 2. ?
  }
}

a();
```

<details>
  <summary>Solution</summary>
  <strong>1. 1<br>2. b</strong>
  <pre>var 키워드로 선언된 변수는 오로지 함수의 코드 블록(함수 몸체)만을 지역 스코프로 인정한다. 또한 자바스크립트는 렉시컬 스코프를 따르므로 함수를 어디서 정의했는지에 따하 상위 스코프를 결정한다.</pre>
</details>

<br>

<pre>3. 함수를 어디서 호출했는지에 따라 함수의 상위 스코프를 결정하는 것을 [1.           ] 함수를 어디서 정의했는지에 다라 함수의 상위 스코프를 결정하는 것을 [2.              ]
</pre>


<details>
  <summary>Solution</summary>
  <strong>1.동적 스코프(dynamic scope)<br>2.렉시컬 스코프(lexical scope)</strong>
</details>