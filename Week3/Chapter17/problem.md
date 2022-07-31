# Chapter 17

<pre>1. 객체 리터럴에 의한 객체 생성 방식은 직관적이고 편하다. 하지만 왜 비효율 적인가 ?</pre>

```js
const circle1 = {
  radius: 5,
  getDiameter() {
    return 2 * this.radius;
  },
};

console.log(circle1.getDiameter()); // 10

const circle2 = {
  radius: 10,
  getDiameter() {
    return 2 * this.radius;
  },
};

console.log(circle2.getDiameter()); // 20
```

<details>
  <summary>Solution</summary>
  <strong>동일한 프로퍼티를 갖는 객체를 여러 개 생성해야하는 경우 매번 같은 프로퍼티를 기술해야하기 때문입니다.</strong>
</details>

<br>

<pre>2. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

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

<pre>3. 생성자 함수의 인스턴스 생성 과정 3단계를 서술하시오.</pre>

<details>
  <summary>Solution</summary>
  <strong>1. 인스턴스 생성과 this 바인딩</strong><br><strong>2. 인스턴스 초기화<br>3. 인스턴스 반환</strong>
</details>

<br>

<pre>4. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```j
function Circle(side) {
  this.side = side;

  return { radius: 10 };
}

function Square(side) {
  this.side = side;

  return 100;
}

function Triangle(side) {
  this.side = side;

  return;
}

const circle = new Circle(1);
console.log(circle); // 1. ?

const square = new Square(4);
console.log(square); // 2. ?

const triangle = new Triangle(3);
console.log(triangle); // 3. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. {radius: 10}</strong><br><strong>2. Square {side: 4}<br>3. Triangle {side: 3}</strong>
  <pre>생성자 함수 내부의 처리가 끝나면 인스턴스가 바인딩된 this가 암묵적으로 반환이 된다.<br>1번은 Circle생성자 함수는 this가 아닌 다른 객체가 명시적으로 return하고 있어 this가 반환되지 않는다.<br>2번은 Square생성자 함수가 원시값인 100을 return하여 원시값은 무시되고 this가 반환된다.<br>3번은 Triangle생성자 함수가 undefined를 반환하고 있어 이 역시 원시값이므로 this가 반환된다.</pre>
</details>

<br>

<pre>5. 생성자 함수가 new 연산자 없이 호출되는 위험성을 회피하기위한 기능은 무엇인가?</pre>


<details>
<summary>Solution</summary>
<strong>new.target</strong>
<pre>사용예:

```js
function Circle(radius) {
    if (!new.target) {
        return new Circle(radius);
    }
    this.radius = radius;
    this.getDiameter = function () {
        return 2 * this.radius;
    }
}
// new 연산자 없이 생성자 함수를 호출하여도 new.target을 통해 생성자 함수로서 호출된다.
const circle = Circle(5); 
console.log(circle.getDiameter()); // 10
```
다만, new.target은 ES6에서 도입된 최신 문법으로 IE에서는 지원하지않음을 유의해야한다.
</pre>
</details>
