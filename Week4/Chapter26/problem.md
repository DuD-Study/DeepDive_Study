# Chapter 26

<pre>1. 즉시 실행 함수를 화살표 함수 버전으로 바꿔보세요.</pre>

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


<pre>2. O X 예상해보세용.</pre>

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
