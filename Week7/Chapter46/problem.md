# Chapter 46

<pre>1. 다음의 출력값을 예상해보자.</pre>

```js
function* introduce() {
  const first = yield "안녕하세요.";
  const second = yield `${first} 입니다.`;
  return `${second} 반갑습니다.`;
}

const generator = introduce();

generator.next("조강훈").value; // 1.
generator.next("만나서").value; // 2.
generator.next(); // 3.
generator.next(); // 4.
```

<details>
  <summary>Solution</summary>
  <pre>1.안녕하세요 <br>
2.만나서 입니다 <br>
3.{value: 'undefined 반갑습니다.', done: true} <br>
4.{value: undefined, done: true}</pre>
<pre>876p 참조</pre>
</details>

<br>

<pre>2. 다음 코드는 값이 반환되는 소요시간이 6초입니다. 소요시간이 3초가 되게 변경해주세요.</pre>

```js
async function foo() {
  const a = await new Promise((resolve) => setTimeout(() => resolve(1), 3000));
  const b = await new Promise((resolve) => setTimeout(() => resolve(2), 2000));
  const c = await new Promise((resolve) => setTimeout(() => resolve(3), 1000));

  console.log([a, b, c]); // [1,2,3]
}

foo(); // 약 6초 소요 됨.
```

<details>
  <summary>Solution</summary>
  <pre>
async function foo() {
  const result = await Promise.all([
    new Promise((resolve) => setTimeout(() => resolve(1), 3000)),
    new Promise((resolve) => setTimeout(() => resolve(2), 2000)),
    new Promise((resolve) => setTimeout(() => resolve(3), 1000))
  ]);
  console.log(result); // [1,2,3]
}

foo(); // 약 3초 소요 됨.

</pre>
<strong>👉🏻 await키워드는 프로미스의 상태가 settled가 되면 프로미스가 resolve한 처리 결과를 반환한다. 모든 프로미스에 await 키워드를 사용하게 되면 settled상태가 될때 까지 기다려야하기 때문에 서로 연관이 없는 비동기 처리는 Promise.all을 사용하여 병렬적으로 실행하는 것이 좋다. </strong>
</details>

<br>
