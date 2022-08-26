# Chapter 47

<pre>1. 출력 값을 예상해보자.</pre>

```js
try {
  new Error("ERROR!");
} catch (err) {
  console.log(err);
} finally {
  console.log("finally");
}
```

<details>
  <summary>Solution</summary>
finally
  <pre>Error 생성자 함수로 에러 객체를 생성한다고 에러가 발생하진 않는다.<br>
throw new Error("ERROR!") 형식으로 에러를 발생 시켜줘야한다.</pre>
</details>

<br>

<pre>2. 빈칸에 들어갈 프로퍼티를 작성하고, 해당 프로퍼티의 특징을 설명하세요.</pre>

<pre>Error 생성자 함수가 생성한 에러 객체는 [1.    ]프로퍼티와 [2.    ]프로퍼티를 갖는다.</pre>

```js
const error = new Error("invalid");
```

<details>
  <summary>Solution</summary>
  <strong>1. message 2. stack</strong>
  <pre>message 프로퍼티의 값은 Error생성자 함수에 인수로 전달한 에러 메세지이고, <br>stack 프로퍼티의 값은 에러를 발생시킨 콜스택의 호출 정보를 나타내는 문자열이며 디버깅 목적으로 사용합니다.</pre>
</details>

<br>
