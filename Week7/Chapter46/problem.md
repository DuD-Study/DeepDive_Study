# Chapter 46

<pre>1. 다음의 출력값을 예상해보자.</pre>

```js
function* introduce() {
    const first = yield "안녕하세요.";
    const second = yield `${first} 입니다.`;
    return `${second} 반갑습니다.`;
}

const generator = introduce()

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
