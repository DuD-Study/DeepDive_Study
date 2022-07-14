# Chapter 7

<pre>1. 피연산자를 숫자 타입을 변환하여 반환하시오.</pre>

```js
console.log(typeof '100')          // string
console.log(typeof 1.[    ]('100'))    // Number
console.log(typeof 2.[    ]('100'))    // Number
console.log(typeof 3.[    ]'100')      // Number
```

   <details>
      <summary>Solution</summary>
        <strong>1.Number</strong><br>
        <strong>2.parseInt</strong><br>
        <strong>3.+</strong>
   </details>

<br>
<br>
<br>

<pre>2. 아래 코드에서 보듯이 타입이 자동으로 전환되어 연산을  수행하기도 하는데, 이것을 [          ] 또는 [          ]라고 한다. </pre>

```js
console.log(1 + true); // 2
console.log(1 + false); // 1
console.log(1 + null); // 1
console.log(+undefined); // NaN
console.log(5 == "5"); // true
```

   <details>
      <summary>Solution</summary>
        <strong>암묵적 타입 변환(implicit coercion), 타입 강제 변환(type coercion)</strong>
   </details>

<br>
<br>
<br>

<pre>3. 동등 비교 연산자(==)와 일치비교 연산자(===)의 차이는 ?</pre>

   <details>
      <summary>Solution</summary>
        <strong>동등 비교 연산자는 비교할때 먼저 암묵적 타입 변환을 통해 타입을 일치시키고 값을 비교한다.<br>하지만 일치 비교 연산자는 암묵적 타입 변환을 하지않고 비교를 한다. </strong>
   </details> 
<br>
<pre>4. 아래 코드의 결과값은? </pre>

```js
var x = 10,
  result;

result = x++;
console.log(result, x);
result = ++x;
console.log(result, x);
result = x--;
console.log(result, x);
result = --x;
console.log(result, x);
```

   <details>
      <summary>Solution</summary>
        <strong>1. 10, 11 선할당 후증가 <br>
        2. 12, 12 선증가 후할당 <br>
        3. 12, 11 선할당 후감소 <br>
        4. 10, 10 선감소 후할당 </strong>
   </details> 
   <br>
<pre>5. 아래 코드의 결과값은? </pre>

```js
var x;
x = 10;
x *= 5;
console.log(x);
```

   <details>
      <summary>Solution</summary>
        <strong> x = 50  &nbsp//&nbsp x = x * 5 </strong>
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
<pre>7. 결과를 예측해 보세요.</pre>

```js
let x = 1;
console.log(-x);
console.log(x);
console.log(++x);
console.log(x--);
console.log(x);
```

<details>
   <summary>Solution</summary>
      <strong>-1, 1, 2, 2, 1</strong>
      <pre>[해설]<br/> - 단항 산술 연산자 -은 양수를 음수로, 음수를 양수로 반전한 값을 반환합니다. 또한 부수효과가 없으므로 x의 값은 변환하지 않습니다. <br/> - 전위 증가 함수 ++은 먼저 피연산자의 값을 증가 시킨 후, 다른 연산을 수행합니다. <br/> - 후위 감소 연산자 --은 먼저 다은 연산을 수행한 후, 피연산자의 값을 감소 시킴니다.</pre>

</details>

<br>
<pre>8. 다음과 같이 0과 NaN은 일치 비교 연산자로 정확한 평가가 되지 않습니다. ES6에 도입된 이 메서드는 0과 NaN의 정확한 비교 결과를 반환하는데 이 메서드는 무엇일까요.</pre>

```js
console.log(-0 === +0); // true
console.log(NaN === NaN); // false
```

<details>
   <summary>Solution</summary>
      <strong>Object.is</strong>
      <pre>[해설]<br/> Object.is(-0,+0), Object.is(NaN, NaN) 각각 false, true를 반환합니다.</pre>
</details>

<br>

<pre>9. 다음 결과를 예측하세요.</pre>

```js
let num = 10;
5 == num / 2 && (2 + 2 * num).toString() === "22";
```

<details>
   <summary>Solution</summary>
      <strong>true</strong>
      <pre>[해설]<br/>1. 5 == num / 2 && (2 + 2 * num).toString() === "22";
2. 5 == num / 2 && (22).toString() === "22";
3. 5 == num / 2 && "22" === "22";
4. 5 == 5 && "22" === "22";
5. true && "22" === "22";
6. true && true;
7. true;</pre>
</details>

<br>
