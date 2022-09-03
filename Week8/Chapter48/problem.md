# Chapter 48

<pre>1. 모듈은 공개가 필요한 자산에 한정하여 명시적으로 선택적 공개가 가능한데, 이를 [   1   ]라고 하고
모듈 사용자는 모듈이 공개한 자산 중 일부 또는 전체를 선택해 자신의 스코프 내로 불러들여 재사용할 수 있는데 이를 [   2   ]라한다.</pre>

<details>
  <summary>Solution</summary>
<strong>1. export<br>
2. import</strong>
</details>

<br>

<pre>2. 다음 코드를 보고 출력값을 예상하세요.</pre>

```html
<script type="module" src="foo.mjs"></script>
```

```js
// foo.mjs
var x = "foo";
console.log(x); // 1. ?
console.log(window.x); // 2. ?
```

<details>
  <summary>Solution</summary>
<strong>1. foo<br>
2. undefined</strong>
<pre>x 변수는 전역 변수가 아니며 window 객체의 프로퍼티도 아니다.</pre>
</details>

<br>

<pre>3. 다른 모듈에서 [   1   ]한 식별자를 자신의 모듈 스코프 내부로 로드하려면 [   2   ] 키워드를 사용한다. 다른 모듈이 [   3   ]한 식별자 이름으로 [   4   ]해야 하며 ESM의 경우 파일 확장자를 생략할 수 없다. </pre>

<details>
  <summary>Solution</summary>
<strong>1. export<br>
2. import</strong><br>
<strong>3. export<br>
<strong>4. import<br>
</details>

<br>

<pre>4. ESM 이란? </pre>

<details>
  <summary>Solution</summary>
<strong>답: IE를 제외한 대부분의 브라우저에서 사용할 수 있는 ES6 모듈. (ES Module)<br>
</details>

<br>

<pre>5. 모든 자바스크립트 파일은 하나의 전역을 공유한다. 분리된 자바스크립트 파일들의 전역 변수가 중복되는 등의 문제가 발생할 수 있다. -> 이런 방식으로는 모듈 구현이 불가하다. 그렇다면 브라우저 환경에서는 어떻게 해야 모듈을 사용할 수 있을까? </pre>

<details>
  <summary>Solution</summary>
<strong>답:  'Common JS / AMD를 구현한 모듈 로더 라이브러리를 사용'하여 구현 가능.
<br>
</details>

<br>
