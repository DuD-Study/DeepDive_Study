# Chapter 22

<pre>1. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```js
function foo() {
  console.log(this);
}

const a1 = foo();
console.log(a1); // 1. ?

const a2 = { foo };
console.log(a2.foo()); // 2. ?

const a3 = new foo();
console.log(a3); // 3. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. Window</strong><br><strong>2. a2({foo: ƒ})<br>3. a3(foo {})</strong>
  <pre>this바인딩은 함수가 호출 방식에 따라 동적으로 결정되는데,<br>1번은 일반함수로 foo를 호출하여 this에 전역 객체인 Window를 가리키게 된다.<br>2번은 a2에 foo함수를 프로퍼티 축약 표현으로 추가했기 때문에 메서드를 호출한 객체 즉, a2가 this에 바인딩된다.<br>3번은 new연산자로 foo함수를 생성자 함수로 호출하였기 때문에 해당 인스턴스인 a3이 this에 바인딩된다.</pre>
</details>

<br>

<pre>2. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```js
const fish = {
  name: "goldfish.",
  getName() {
    console.log(`${this.name}`);
  },
};

const getName = fish.getName;
getName(); // ?
```

<details>
  <summary>Solution</summary>
  <strong>''(브라우저 환경에서 window.name)</strong>
  <pre>fish객체의 getName 프로퍼티는 독립적으로 존재하여 일반 변수에 할당하여 일반 함수로 호출할 수 있다.<br>일반 함수 호출에서 this는 전역객체를 가리키므로 브라우저 환경에서 window.name을 반환한다.</pre>
</details>

<pre>3. this를 원하는 객체로 바인딩하며 함수를 호출하게 해주는 함수 메서드 3가지는 무엇인가? </pre>

<details>
<summary>Solution</summary>
<strong>apply, call, bind</strong></details>


<pre>4. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```js
function makeUser() {
  return {
    name: "John",
    ref: this
  };
};

let user = makeUser();

alert( user.ref.name ); // 결과가 어떻게 될까요?
```

<details>
  <summary>Solution</summary>
  <strong>에러가 발생합니다 - </strong>Error: Cannot read property 'name' of undefined
  <pre>에러가 발생하는 이유는 this 값을 설정할 땐 객체 정의가 사용되지 않기 때문입니다. this 값은 호출 시점에 결정됩니다.
위 코드에서 makeUser() 내 this는 undefined가 됩니다. 메서드로써 호출된 게 아니라 함수로써 호출되었기 때문입니다.
this 값은 전체 함수가 됩니다. 코드 블록과 객체 리터럴은 여기에 영향을 주지 않습니다.
따라서 ref: this는 함수의 현재 this 값을 가져옵니다.
this의 값이 undefined가 되게 함수를 다시 작성하면 다음과 같습니다.
</pre>

```js
function makeUser(){
  return this; // 이번엔 객체 리터럴을 사용하지 않았습니다.
}

alert( makeUser().name ); // Error: Cannot read property 'name' of undefined
```
<pre>
보시다시피 alert( makeUser().name )와 위쪽에서 살펴본 alert( user.ref.name )의 결과가 같은 것을 확인할 수 있습니다.
에러가 발생하지 않게 하려면 코드를 다음과 같이 수정하면 됩니다.</pre>

```js
function makeUser() {
  return {
    name: "John",
    ref() {
      return this;
    }
  };
};

let user = makeUser();

alert( user.ref().name ); // John
```

<pre>이렇게 하면 user.ref()가 메서드가 되고 this는 . 앞의 객체가 되기 때문에 에러가 발생하지 않습니다.</pre>

</details>

<pre>4. 어떻게 출력되고 왜 그렇게 되는가? </pre>

```js
var value = 1;

const ojb = {
  value : 100,
  foo() {
    console.log("foo's this : " , this); //?
    console.log("foo's this.value : " , this.value) //?
  function bar() {
    console.log("bar's this: ", this); //?
    console.log("bar's this.value : " , this.value )
  }
  bar();
  }

}
```
<details>
<summary>Solution</summary>
<strong>{value: 100, foo: f } , 100 , window , 1</strong>
<pre> 중첩 함수도 일반함수로 호출되면 this에는 전역 객체가 바인딩되기때문
</pre>
</details>