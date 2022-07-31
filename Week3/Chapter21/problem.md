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
