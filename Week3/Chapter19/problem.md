# Chapter 19

<pre>1. 프로토타입 체인의 최상위에 위치하는 객체는 언제나 [       ]이다. 따라서  모든 객체는 [       ]을 상속받는다.<br> [       ]을 프로토타입 체인의 종점이라 하며, [       ]의 [[prototype]] 내부 슬롯의 값은 null이다.</pre>

<details>
  <summary>Solution</summary>
  <strong>Object.prototype</strong>
  <pre>프로토타입 체인의 종점인 Object.prototype에서도 프로퍼티를 검색할 수 없는 경우 undefined를 반환한다. 이때 에러가 발생하지 않는 것에 주의하자!</pre>
</details>

<br>

<pre>2. 아래의 코드를 보고 실행 결과를 예측하시오.</pre>

```js
const Person = (function (){
  function Person(name){
    this.name = name;
  }

  Person.prototype = {
    sayHello() {
      console.log('Hi~');
    }
  };

  return Person;
}());

const me = new Person('zooyaho');

console.log(me.constructor === Person); // 1. ?
console.log(me.constructor === Object); // 2. ?

console.log(me instanceOf Person); // 3. ?
console.log(me instanceOf Object); // 4. ?
```

<details>
  <summary>Solution</summary>
  <strong>1. false<br>2. true<br>3. true<br>4. true</strong>
  <pre>프로토타입으로 교체한 객체 리터럴에는 constructor프로퍼티가 없기때문에 1번에 답은 false이다.<br>모든 객체는 Object.prototype을 상속받기 때문에 2번에 답은 true이다.<br>instanceOf연산자는 프로토타입의 constructor 프로퍼티가 가리키는 생성자 함수를 찾는것이 아닌<br>생성자 함수의 prototype에 바인딩된 객체가 프로토타입 체인 상에 존재하는지 확인하기 때문에<br>3,4번의 답은 true이다.</pre>
</details>

<br>

<pre>3. [    ] 프로퍼티/메서드는 생성자 함수로 인스턴스를 생성하지 않아도 참조/호출할 수 있는 프로퍼티/메서드를 말한다.</pre>

```js
function Foo() {}

Foo.x = function () {
  console.log("x");
};

Foo.x(); // x
```

<details>
  <summary>Solution</summary>
  <strong>정적(static)</strong>
  <pre>인스턴스/프로토타입 내에서 this를 사용하지 않는 메서드는 정적 메서드로 변경할 수 있다.</pre>
</details>

<br>

<pre>4. 아래의 예제를 보고 접근자 프로퍼티를 사용하여 프로토타입에 접근하는 이유를 서술하시오.</pre>

```js
const parent = {};
const child = {};

child.__proto__ = parent;
parent.__proto__ = child;
```

<details>
  <summary>Solution</summary>

  <pre>프로토타입에 접근하기 위해 접근자 프로퍼티를 사용하는 이유는 상호 참조에 의해 프로토타입 체인이 생성되는 것을 방지하기 위해서이다.이러한 코드가 에러 없이 정상적으로 처리되면 서로가 자신의 프로토타입이 되는 비정상 적인 프로토타입 체인이 만들어지기 때문에 proto 접근자 프로퍼티는 에러를 발생시킨다.</pre>
</details>

<pre>5. 아래의 빈칸을 알맞은 단어로 채우시오.</pre>
<div align="center">
객체는 [①] 데이터와 [②]을 하나의 논리적인 단위로 묶은 복합적인 자료구조라고 할 수 있다.
이때 객체의 [①]를 [③], [②]를 [④]라 부른다.
</div>

<details>
<summary>Solution</summary>
<strong>①: 상태<br>②: 동작<br>③: 프로퍼티<br>④: 메서드</strong>
</details>

<pre>6. 다음 코드의 실행결과를 예측해보시오.</pre>
```js
const obj = {};
const parent = {x : 1};

Object.setPrototypeOf(obj, parent);

console.log(obj);
```

<details>
<summary>Solution</summary>
<strong>{}</strong>
<pre>obj의 프로토타입에 x: 1이 추가 되는 것이지 obj 자체가 변하는 것은 아니다.
위의 코드에서 Object.getPrototypeOf(obj)를 실행해보자.</pre>
</details>

