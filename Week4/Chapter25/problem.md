# Chapter 25

<pre>1. 다음 생성자 함수를 클래스로 만들어보자, 똑같이  </pre>

```js
function Intro(name, MBTI) {
  this.name = name;
  this.MBTI = MBTI;

  Intro.prototype.sayHi = function () {
    console.log(
      `Hi my name is ${this.name}, and btw What's your MBTI? mine is ${this.MBTI}`
    );
  };
}

const me = new Intro("jeongmin", "ESTP");
me.sayHi();
```

<details>
  <summary>Solution</summary>

```js
class Intro {
  constructor(name, MBTI) {
    this.name = name;
    this.MBTI = MBTI;
  }

  sayHi() {
    console.log(
      `Hi my name is ${this.name}, and btw What's your MBTI? mine is ${this.MBTI}`
    );
  }
}

const me = new Intro("jeongmin", "ESTP");
me.sayHi();
```

</details>

<br>

<pre>2. 다음 코드를 실행하면 error를 발생시킨다. 이유를 설명하시오. (두 error는 같은 이유의 error를 발생 시킨다.)</pre>

```js
const Person = class MyClass {};

console.log(MyClass); // Error
const you = new MyClass(); // Error
```

<details>
<summary>Solution</summary>
<Strong>ReferenceError: MyClass is not defined</Strong>
<pre>클래스 표현식으로 정의된 클래스의 경우 기명 함수 표현식과 마찬가지로<br>클래스 표현식에서 사용한 클래스 이름은 외부코드에서 접근 불가능하기 때문이다.</pre>
</details>

<br>
