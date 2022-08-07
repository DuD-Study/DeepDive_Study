# Chapter 24

<pre>1. 모든 함수는 상위 스코프를 기억하므로 이론적으로 모든 함수는 클로저인데,
   일반적으로 모든 함수를 클로저라고 하지 않는다. 다음 코드를 보고 클로저가 아닌 이유는 ?</pre>

```js
function foo() {
      const x = 1;
      const y = 2;

      function bar() {
        const value = 3;
        console.log(2*value);
      }

      return bar;
    }

    const getDouble = foo();
    getDouble();
```



<details>
  <summary>Solution</summary>
  <pre>중첩함수가 외부함수, 즉 상위 스코프 식별자를 참조하지 않으면 클로저라고 하지않는다.</pre>
</details>

<br>
<pre>2. 코드의 실행결과와 이유를 설명하시오.</pre>

```js
  var funcs = [];
  for ( var i = 0 ; i < 3 ; i++>){
    funcs[i] = function(){return i;}
  }
  for( var j = 0; j< funcs.length; j++){
    console.log(funcs[j]());
  }

```



<details>
  <summary>Solution</summary>
  <pre>3이 3번 찍힙니다
  왜냐하면 for문의 변수 i 는 함수 레벨 스코프를 갖기때문에 전역변수이므로 i 에는 0 , 1 , 2가 순차적으로 할당된다.
  추후 호출시에는 전역변수 i를 참조하기때문에 3이 출력된다.
  0,1,2가 출력되게끔 하려면 let을 사용하거나 클로저 개념을 활용해보자
   </pre>
</details>

<br>

<pre>3. 아래 코드의 출력값을 예상해보고, 원하는대로 동작하게 하려면 어떻게 수정해야할까?</pre>
```js
function createIncrement() {
  let cnt = 0;
  function increment() { 
    cnt++;
  }
  let message = cnt;
  function log() {
    console.log(message);
  }
  
  return [increment, log];
}
const [increment, log] = createIncrement();
increment(); 
increment(); 
increment(); 
log();
```

<details>
<summary>Solution</summary>
<strong>출력값 : 0</strong>
기존 코드에서 log는 createIncrement 스코프의 message를 참조하고있으므로, 0이 찍히게된다.
따라서 아래의 코드처럼 cnt를 직접출력하거나, message를 increment내에서 수정하는 방법도 있겠다.

```js
function createIncrement() {
  let cnt = 0;
  function increment() { 
    cnt++;
  }
  function log() {
    console.log(cnt);
  }
  
  return [increment, log];
}
const [increment, log] = createIncrement();
increment(); 
increment(); 
increment(); 
log();
```

</details>
