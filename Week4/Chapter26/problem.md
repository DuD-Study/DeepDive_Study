# Chapter 26

<pre>1. 다음 코드의 실행결과를 예측하시오.</pre>

```js
function foo(a, b, ...c) {
  console.log(a); // 1. ?
  console.log(b); // 2. ?
  console.log(c); // 3. ?
}
foo(1, 2, 3, 4, 5);
console.log(foo.length); // 4. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. 1<br>2. 2<br>3. [3, 4, 5]<br>4. 2</strong>
  <pre>먼저 선언된 매개변수에 할당된 인수를 제외한 나머지 인수들로 구성된 배열이 Rest파라미터에 할당된다.<br> Rest파라미터는 함수 객체의 length 프로퍼티에 영향을 주지 않는다. </pre>
</details>

<br>
