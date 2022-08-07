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

<pre>2. 즉시 실행 함수를 화살표 함수 버전으로 바꿔보세요.</pre>

```js
(function(count) {
  for(let i=0; i<count; i++)
    console.log("I am IIFE");
})(3);
```

<details>
  <summary>Solution</summary>
  <strong>

  ```js
  ((count) => {
    for(let i=0; i<count; i++)
    console.log("I am IIFE");
  })(3)
  ```
  </strong>
</details>

<br>


<pre>3. O X 예상해보세용.</pre>

|ES6 함수의 구분|constructor|prototype|super|arguments|
|:-:|:-:|:-:|:-:|:-:|
|일반함수|O|1.|X|O|
|메소드|2.|X|3.|O|
|화살표 함수|4.|X|X|X|

<details>
  <summary>Solution</summary>
  <strong>
  1.O : p.470 쪽 봐주세요.<br>
  2.X : 메소드는 non-constructor 입니다<br>
  3.O : 메소드는 자신을 바인딩한 객체를 가르키는 내부슬롯 [[HomeObject]]를 갖게되는데, super 키워드는 이를 갖고 있는 메소드만 사용할 수 있다. <br>
  4.X : 에로우 함수는 non-constructor 입니다<br>  
  </strong>

</details>

<br>
<pre>4. 아래 코드의 결과와 그 이유는?</pre>

```js
const counter = {
  num : 1,
  increase : () => ++this.num
}

console.log(counter.increase());
```

<details>
  <summary>Solution</summary>
  <strong>
  <pre>NaN
  화살효 함수는 this 바인딩을 갖지 않기 때문에 call, apply, bind 메서드를 사용해도 화살표 함수 내부의 this를 교체할 수 없다. + 이러한 이유들로 일반적으로 메서드를 정의할때는 화살표 함수를 쓰지 않는다.</pre>
  </strong>
</details>

<br>