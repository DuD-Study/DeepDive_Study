# Chapter 49

<pre>1. 구형 브라우저에서는 화살표 함수나 지수연산자를 지원 안할 수 있다.
이 때 대표적으로 쓰이는 컴파일러는 [   1   ]이고, ES5 사양의 소스코드로 변환할 수 있다. [   1   ]을 사용하려면,
[      2      ]도 설치해야하는데, 함께 사용하는 [   1   ] 플러그인을 모아 둔 것이다.</pre>

<details>
  <summary>Solution</summary>
<strong>1. Babel<br>
2. @babel/preset-env(바벨 프리셋)</strong>
</details>

<br>

<pre>2. 다음은 npm scripts에 Babel CLI 명령어를 등록한 것이다.
사용한 옵션의 의미를 설명하세요.
</pre>

```
// package.json
"scripts": {
  "build": "babel src/js -w -d dist/js"
}
```

<details>
  <summary>Solution</summary>
<pre>1. -w: 타깃 폴더에 있는 모든 자바스크립트 파일들의 변경을 감지하여 자동으로 트랜스파일한다.(--watch옵션의 축약형)
2. -d: 트랜스파일링된 결과물이 저장될 폴더를 지정한다. 만약 지정된 폴더가 존재하지 않으면 자동 생성된다.(--out-dir 옵션의 축약형)</pre>
</details>

<br>

<pre>3. [   1   ]인 Werbpack을 통해 [   2   ]인 Bable을 로드하여 최산 버전 ES 6+ / ES.NEXT 소스코드를 구형 브라우저인 IE같은 환경에서도 동작할 수 있도록 ES5 사양의 소스코드로 [   3   ]할 수 있다. </pre>

<details>
  <summary>Solution</summary>
<strong>1. 모듈 번들러<br>
2. 트랜스파일러</strong><br>
<strong>3. 트랜스파일링<br>
</details>

<br>

<pre>4. [   1   ]은 의존관계에 있는 자바스크립트, css, 이미지 등의 리소스들을 하나의 파일로 번들링하는 모듈 번들러이다. [   1   ]을 사용하면 의존 모듈이 하나의 파일로 번들링하므로 HTML 파일에서 script 태그로 여러개의 자바스크립트 파일을 로드해야 하는 번거러움도 사라진다. </pre>

<details>
  <summary>Solution</summary>
<strong>답: webpack<br>
</details>

<br>

<pre>5. babel의 @babel-polyfill은 개발 환경에서만 사용하는 것이 아니라 실제 운영 환경에서도 사용해야한다.	ES6의 import 구문을 사용하는 경우에는 진입점의 선두에서 먼저 [   1   ]을 로드하도록 한다. </pre>

<details>
  <summary>Solution</summary>
<strong>답: 폴리필<br>
</details>

<br>
