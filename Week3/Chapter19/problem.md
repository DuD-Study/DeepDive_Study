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
