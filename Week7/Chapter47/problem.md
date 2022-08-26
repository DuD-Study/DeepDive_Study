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


<pre>3. 빈칸에 뭐가 들어갈지 생각해보세요.</pre>

<pre>기본적으로 에러 처리를 구현하는 방법은 크게 두 가지가 있다. querySelector나 Array#find 메소드처럼 예외적인 상황이 발생하면 반환하는 값을 [  1   ]문이나 [   2   ] 또는 [   3   ]연산자를 통해 확인해서 처리하는 방법과 에러 처리 코드를 미리 등록해 두고 에러가 발생하면 에러 처리 코드로 점프하도록 하는 방법이 있고, try...catch...finally가 두번째 방법이다.</pre>

<details>
  <summary>Solution</summary>
  <strong>1. if<br/>2. 단축평가<br/>3. 옵셔널 체이닝<br/>Page.888</strong>
  
</details>

<br>