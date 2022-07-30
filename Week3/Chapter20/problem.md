# Chapter 20

<pre>1. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```js
(function myName(name) {
  "use strict";

  name = "zooyaho";
  console.log(name); // 1. ?
  console.log(arguments); // 2. ?
})("lee");
```

<details>
  <summary>Solution</summary>
  <strong>1. zooyaho<br>2. lee</strong>
  <pre>strict mode에서 매개변수에 전달된 인수를 재할당하여 변경해도 arguments 객체에 반영되지 않는다.</pre>
</details>
