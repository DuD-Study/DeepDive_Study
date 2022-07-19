# Chapter 15

<pre>1. 아래의 코드를 보고 실행 결과를 예측하시오.
</pre>

```js
var x = 1;
y = 2;
let z = 3;

console.log(window.x); // 1. ?
console.log(y); // 2. ?
console.log(window.z); // 3. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. 1<br>2. 2<br>3.undefined</strong>
  <pre>1. var 키워드로 선언된 전역변수는 전역객체의 프로퍼티로 추가된다. 따라서 브라우저의 전역객체를 가리키는 window의 프로퍼티로 추가된다.<br>2. 선언하지 않은 변수에 값을 할당한 암묵적 전역 변수는 전역객체 window의 프로퍼티가 된다. 전역 객체의 프로퍼티를 참조할 때 window를 생략할 수 있다.<br>3. let으로 선언된 전역 변수는 전역객체 window의 프로퍼티가 되지 않음.</pre>
</details>

<br>
