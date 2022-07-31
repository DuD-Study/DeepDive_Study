# Chapter 20

<pre>1. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```js
(function myName(name) {
  "use strict";

  name = "zooyaho";
  console.log(name); // 1. ?
  console.log(arguments); // 2. ?
  console.log(this); // 3. ?
})("lee");
```

<details>
  <summary>Solution</summary>
  <strong>1. zooyaho<br>2. lee<br>3. undefined</strong>
  <pre>strict mode에서 매개변수에 전달된 인수를 재할당하여 변경해도 arguments 객체에 반영되지 않는다.
<br>strict mode에서 함수를 임반함수로서 호출하면 this에 undefined가 바인딩 된다.</pre>
</details>

<br>

<pre>2. 아래의 코드를 보고 빈칸에 들어갈 알맞은 단어를 쓰십시오.</pre>

```js
<!DOCTYPE html>
<html>
  <body>
    <script>
      'use strict';
    </script>
    <script>
      x = 1;	// 에러가 발생하지 않음
      console.log(x);	// 1
    </script>
    <script>
      'use strict';
      y = 1;	// ReferenceError: y is not defined
    </script>
  </body>
</html>
```
<pre>[  1  ]에 적용한 strict mode는 스크립트 단위로 적용되기 때문에 피하는 것이 좋다. strict mode와 non-strict mode를 혼용하는 것은 오류를 발생시킬 수 있으며
특히 외부 라이브러리를 사용하는 경우 라이브러리가 non-strict mode인 경우도 있다. 그렇기 때문에 [   2   ]로 스크립트 전체를 감싸서 스코프를 구분하고 [   2   ]의 선두에 strict mode를 적용하는 것이 바람직하다.  </pre>

<details>
  <summary>Solution</summary>
  <strong>1. 전역 <br>2. 즉시 실행 함수</strong>
</details>

