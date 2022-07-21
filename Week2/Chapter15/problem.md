# Chapter 15

<pre>1. 아래의 코드를 보고 실행 결과를 예측하시오.
</pre>

```js
var x = 1;
y = 2;
console.log(z); // 1. ?
let z = 3;

console.log(window.x); // 2. ?
console.log(y); // 3. ?
console.log(window.z); // 4. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. ReferenceError</strong><br><strong>2. 1<br>3. 2<br>4.undefined</strong>
  <pre>1. let과 const키워드로 선언한 변수는 변수 호이스팅이 발생하지 않는 것 처럼 동작한다. <br>2. var 키워드로 선언된 전역변수는 전역객체의 프로퍼티로 추가된다. 따라서 브라우저의 전역객체를 가리키는 window의 프로퍼티로 추가된다.<br>3. 선언하지 않은 변수에 값을 할당한 암묵적 전역 변수는 전역객체 window의 프로퍼티가 된다. 전역 객체의 프로퍼티를 참조할 때 window를 생략할 수 있다.<br>4. let으로 선언된 전역 변수는 전역객체 window의 프로퍼티가 되지 않음.</pre>
</details>

<br>

<pre>2. 아래 코드를 보고 실행 결과를 예측하시요. 
</pre>

```js
var i = 10;
let j = 2;

function cal(a,b){  
  return a*b**2;
}

for(var i = 1; i <= 5 ; i++){
  console.log(i);
}

console.log(cal(i,j));
```

<details>
  <summary>Solution</summary>
  1<br>2<br>3<br>4<br>5<br>24
  <pre>var i는 for문의 블록스코프에서 재선언 됬을때 10이라는 값을 잃고, 재선언된 1부터 시작해 for문이 끝나고 난 뒤, 생명주기가 다하지않고 6이라는 값이 유지되며, 애플리케이션이 끝날때까지 유지됩니다.</pre>
</details>

<br>
<pre>3. 상수를 만들때 어떻게 만들어야 하며 상수로 선언된 객체값을 바꿀수 있나요?
</pre>

<details>
  <summary>Solution</summary>
  <pre>Const 를 이용하며 대문자 + _(언더바) 를 이용하여 만들며, 상수 키워드로 선언된 객체는 값을 변경할 수 있습니다.</pre>
</details>

<br>
<pre>4. let 키워드로 선언한 변수는 [   1   ]와 [   2   ]가 분리되어 진행된다.  즉, 런타임 이전에 자바스크립트 엔진에 의해 암묵적으로 [   1   ]가 먼저 실행되지만 [   2   ]는 변수 선언문에 도달했을 때 실행된다.
</pre>

<details>
  <summary>Solution</summary>
  <strong>1: 선언 단계  2: 초기화 단계</strong>

</details>