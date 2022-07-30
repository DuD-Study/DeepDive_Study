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
