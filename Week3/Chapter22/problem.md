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
