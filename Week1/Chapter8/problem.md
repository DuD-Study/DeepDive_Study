# Chapter 8

<h2 align="center">제어문을 바르게 이해하는 것은 코딩 스킬에 많은 영향을 준다. </h2>
<br>

<pre>1. 자바스크립트는 [    ] 문과 [    ]문 두가지 조건문을 제공한다.</pre>
   <details>
      <summary>Solution</summary>
        <strong>if , switch</strong><br>
   </details> 
<br>

<pre>2. switch문에서 탈출을 의미하는 단어는 ?  </pre>
   <details>
      <summary>Solution</summary>
        <strong>break</strong><br>
   </details> 
<br>

<pre>3. 반복문의 코드를 현 지점에서 중단하고 증감식으로 실행 흐름을 이동시키는 단어는?  </pre>
   <details>
      <summary>Solution</summary>
        <strong>continue</strong><br>
   </details> 
<br>

<pre>4. for문을 활용해서 피보나치 수열의 첫 10개 항을 차례대로 출력하는 프로그램을 작성해 보세요.
[출력] 1 1 2 3 5 8 13 21 34 55
</pre>

<details>
   <summary>Solution</summary>
<pre>
let current = 1;
let previous = 0;
for (let i = 1; i <= 10; i++) {
console.log(current);
let temp = previous;
previous = current;
current = current + temp;
}
</pre>

</details>

<br>

<pre>5. [  ]문은 레이블 문, 반복문(for, for..in, for..of, while, do..while) 또는 switch 문의 코드 블록을 탈출합니다.<br> 이것 외에 [  ]문을 사용한다면 SyntaxError(문법 에러)가 발생합니다.
</pre>

<details>
   <summary>Solution</summary>
      <strong>break</strong>
</details>

<br>

<pre>6. 아래 코드를 삼항 조건 연산자로 바꿔보시오 </pre>

```js
if (score >= 60) {
  result = "합격";
} else {
  result = "불합격";
}
```

   <details>
      <summary>Solution</summary>
        <strong> var result = score >= 60 ? "합격" : "불합격"</strong>
   </details> 

<br>
