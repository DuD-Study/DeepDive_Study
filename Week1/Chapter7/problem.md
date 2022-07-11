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
console.log(1+true);       // 2
console.log(1+false);      // 1
console.log(1+null);       // 1
console.log(+undefined);   // NaN
console.log(5=='5')        // true
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
var x = 10, result;

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
x *= 5
console.log(x)
```

   <details>
      <summary>Solution</summary>
        <strong> x = 50  &nbsp//&nbsp x = x * 5 </strong>
   </details> 
   <br>

<pre>6. 아래 코드를 삼항 조건 연산자로 바꿔보시오 </pre>

```js
if (score >= 60){
   result = "합격"
} else {
   result = "불합격"
}
```

   <details>
      <summary>Solution</summary>
        <strong> var result = score >= 60 ? "합격" : "불합격"</strong>
   </details> 
   
