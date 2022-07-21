# Chapter 16

<pre>1. 모든 객체는 [[Prototype]]이라는 내부 슬롯을 갖는다.<br> 내부 슬롯은 자바스크립트 엔진의 내부 로직이므로 원칙적으로 직접 접근할 수 없지만<br>[[Prototype]] 내부 슬롯의 경우, [      ]를 통해 간접적으로 접근할 수 있다.
</pre>

```js
const o = {};
o.[[Prototype]]; // SyntaxError
o.[     ]; // Object.prototype

```

<details>
  <summary>Solution</summary>
  <strong>__proto__</strong>
</details>

<br>

<pre>2. 아래의 코드를 보고 빈칸을 예측하시오.
</pre>

```js
const person = {
  name: "Lee",
};
person.age = 40;

console.log(Object.getOwnPropertyDescriptor(person, "age"));
```

**출력**

```js
{ value: 40, writable: [1.    ], enumerable: [2.    ], configurable: [3.    ]}
```

<details>
  <summary>Solution</summary>
  <strong>1. true<br>2. true<br>3. true</strong>
  <pre>프로퍼티를 <strong>동적으로 추가하면</strong> [[Writable]], [[Enumerable]], [[Configurable]]의 값은 true로 초기화 된다.</pre>
</details>

<br>

<pre>3. 아래의 코드를 보고 빈칸을 예측하시오.
</pre>

```js
const person = {
  firstName: "Ungmo",
  lastName: "Lee",
};

Object.defineProperty(person, "fullName", {
  set(name) {
    [this.firstName, this.lastName] = name.split(" ");
  },
  enumerable: true,
});
console.log(Object.getOwnPropertyDescriptor(person, "fullName"));
```

**출력**

```js
{get: [1.     ], enumerable: true, configurable: [2.     ], set: ƒ}
```

<details>
  <summary>Solution</summary>
  <strong>1. undefined<br>2. false</strong>
  <pre>Object.defineProperty 메서드로 프로퍼티를 정의할 때 프로퍼티 디스크립터 객체의 프로퍼티를 일부 생략할 수 있다.<br>프로퍼티 디스크립터 객체에서 생략된 어트리뷰트 [[Writable]], [[Enumerable]], [[Configurable]]의 값은 false로 초기화 되며,<br>[[Value]], [[Get]], [[Set]]은 undefined로 초기화 된다.</pre>
</details>

<br>

<pre>4. 아래의 표를 완성해보세요.</pre>
구분 | 메서드 | 프로퍼티추가 | 프로퍼티삭제 | 프로퍼티 값 읽기 | 프로퍼티 값 쓰기 | 프로퍼티 어트리뷰트 재정의 
--|--|--|--|--|--|--
객체 확장 금지 | Object.preventExtensions | 　 | 　 | 　 | 　 | 　  
객체 밀봉 | Object.seal | 　 | 　 | 　 | 　 | 　  
객체 동결 | Object.freeze | 　 | 　 | 　 | 　 | 　  

<details>
<summary>Solution</summary>
구분 | 메서드 | 프로퍼티추가 | 프로퍼티삭제 | 프로퍼티 값 읽기 | 프로퍼티 값 쓰기 | 프로퍼티 어트리뷰트 재정의 
--|--|--|--|--|--|--
객체 확장 금지 | Object.preventExtensions | X | O | O | O | O  
객체 밀봉 | Object.seal | X | X | O | O | X  
객체 동결 | Object.freeze | X | X | O | X | X  
</details>






