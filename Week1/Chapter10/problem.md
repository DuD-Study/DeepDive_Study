# Chapter 10

<h2 align="center">JS를 구성하는 거의 "모든 것"이 객체다.</h2>
<br>

<pre>1. 아래 코드의 결과는? </pre>

```js
var obejct1 = {};
console.log(typeof empty);
```

   <details>
      <summary>Solution</summary>
        <strong>정답은 : object 
        <br>프로퍼티가 없어도 객체는 생성 됩니다.</strong><br>
   </details> 
<br>

<pre>2. 아래 코드의 결과는? </pre>

```js
var person = {
  name: "Kwon",
};
console.log(person.name);
console.log(person["name"]);
console.log(person.age);
```

   <details>
      <summary>Solution</summary>
        <strong> 첫번째, 두번째 은 Kwon이 출력되지만<br> 
        <br>세번째는 객체에 존재하지 않는 프로퍼티에 접근해서 undefined가 반환됩니다.</strong><br>
   </details> 
<br>

<pre>3. 객체의 프로퍼티 접근 방식 중 틀린 것을 고르고 이유를 설명 하시오.
</pre>

```js
let person = {
  name: "lee",
  1: 10
};

1. console.log(person.name); // lee
2. console.log(person[name]); // undefined
3. console.log(person[1]); // 10
4. console.log(person['1']); // 10
```

<details>
   <summary>Solution</summary>
      <strong>2번</strong>
      <pre>[해설]<br/>대괄호 표기법을 사용하는 경우 대괄호 프로퍼티 접근 연산자 내부에 지정하는 프로퍼티 키는 반드시 따옴표로 감싼 문자열이어야 합니다. 따옴표로 감싸지 않으면 자바스크립트 엔진은 식별자로 해석합니다. 2번은 객체에 존재하지 않는 프로퍼티에 접근하였으므로 undefined를 반환합니다.</pre>
</details>

<br>

<pre>4. [  ] 연산자는 객체의 프로퍼티를 삭제합니다. 이때 [  ] 연산자의 피연산자는 프로퍼티 값에 접근할 수 있는 표현식이어야 합니다. <br>만약 존재하지 않는 프로퍼티를 삭제하면 아무런 에러 없이 무시됩니다.
</pre>

<details>
   <summary>Solution</summary>
      <strong>delete</strong>
</details>

<br>
