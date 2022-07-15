# Chapter 9

<h2 align="center">중요한 것은 코드를 예측할 수 있어야 한다는 것이다.</h2>
<br>

<pre>1. 개발자의 의도와는 상관없이 표현식 평가도중 JS엔진에 의해 암묵적으로 타입이 반환<br> 되는 경우가 있는데 이를 [          ] 또는 [          ] 라고 한다.</pre>
   <details>
      <summary>Solution</summary>
        <strong>암묵적 타입 변환, 타입 강제 변환</strong><br>
   </details> 
<br>
<pre>2. 표준 빌트인 생성자 함수는 3가지는 어떤것 일까요?</pre>
   <details>
      <summary>Solution</summary>
        <strong>String , Number, Boolean <br>
        보통 생성자 함수는 new 연산자를 호출하여 사용하는데 위의 3가지 생성자 함수는<br>
        String(1) -> "1" , Number('123') -> 123 , Boolean('x') // true, <br> 
        Boolean('') // false 이런식으로 변환이 가능합니다.</strong><br>
   </details> 
<br>

<pre>3. 'x' && 'y' 의 결과와 이유는?</pre>
   <details>
      <summary>Solution</summary>
        <strong>답은 y <br>
        이유 : 첫번째 x 는 true 로 평가되지만, 이 시점 까지는 표현식을 평가할수 없다.
        두 번째 피연산자까지 표현식의 평가 결과를 결정하는데 평과 결과를 결정할수 없어서<br> 
        논리 연산 결과를 결정하는 두 번째 피연산자 즉 문자열 'y'를 그대로 반환합니다.</strong><br>
   </details> 
<br>

<pre>4. 아래와 같이 자바스크립트엔진은 가급적 에러를 발생시키지 않도록 [  ]타입 변환을 통해 표현식을 평가합니다.
</pre>

```js
"10" + 2; // '102'
5 * 10; // 50
!0; // true
```

<details>
   <summary>Solution</summary>
      <strong>암묵적</strong>
</details>

<br>

<pre>5. 다음 예제를 보고 예측하세요.
</pre>

```js
1. +undefined
2. +[10,20]
3. -null
4. [] + ''
5. [10, 20] + ''
6. +[]
7. +''
```

<details>
   <summary>Solution</summary>
<pre>
1. NaN
2. NaN
3. -0
4. ''
5. '10,20'
6. 0
7. 0
</pre>
<pre>[해설]
단항연산자(+,-)는 피연산자가 숫자 타입의 값이 아니면 숫자타입의 값으로 암묵적 타입 변환을 수행하는데, 빈 문자열(''), 빈 배열([]), null, false는 0,-0으로, true는 1,-1로 변환됩니다. 객체와 빈 배열이 아닌 배열, undefined는 변환되지 않아 NaN이 됩니다.
</pre>
</details>

<br>

<pre>6. 논리합(||) 또는 논리곱(&&) 연산자는 논리 연산의 결과를 결정하는 피연산자를 타입 변환하지 않고 그대로 변환합니다.<br> 이를 [   ]라 한다. [   ]는 표현식을 평가하는 도중에 평가 결과가 확정된 경우 나머지 평가 과정을 생략하는 것을 말합니다.
</pre>

```js
false || "Dog"; // 'Dog'
"cat" && false; // false
```

<details>
   <summary>Solution</summary>
      <strong>단축 평가(short-circuit evaluation)</strong>
</details>

<br>

<pre>7. 문자열 타입이 아닌 값을 문자열 타입으로 변환하는 방법 3가지를 서술하시오.</pre>

<details>
<summary>Solution</summary>
<pre>
1. String 생성자를 호출
2. Object.prototype.toString 메서드를 사용
3. 문자열 연결 연산자를 이용
</pre>
</details>
