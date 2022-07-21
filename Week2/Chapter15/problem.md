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
