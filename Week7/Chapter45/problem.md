# Chapter 45

#### 1. 프로미스는 다음과 같은 진행 상태 정보를 갖습니다. 빈칸을 맞춰주세요.

| 프로미스의 상태 정보 |                 의미                 |         상태 변경 조건          |
| :------------------: | :----------------------------------: | :-----------------------------: |
|       pending        | 비동기처리가 아직 수행되지 않은 상태 | 프로미스가 생성된 직후 기본상태 |
|         (1)          |   비동기 처리가 수행된 상태(성공)    |          (2) 함수 호출          |
|         (3)          |   비동기 처리가 수행된 상태(실패)    |          (4) 함수 호출          |

프로미스는 pending 상태에서 (1), (3) 상태로 변할 수 있는데, 이를 (5) 상태라고 합니다.<br/>
(5) 상태가 일단되면 다른 상태로 변화할 수 없습니다.

<details>
  <summary>Solution</summary>
  <pre><strong>(1) fulfilled</strong>
<strong>(2) resolve</strong>
<strong>(3) rejected</strong>
<strong>(4) reject</strong>
<strong>(5) settled</strong></pre>
</details>

<br>

<pre>2. 아래의 PromiseGet메서드에는 부적절한 URL을 인수로 전달하고 있지만 에러를 캐치하지 못한다. 에러를 캐치할 수 있게 코드를 수정하세요.</pre>

```js
PromiseGet("https://...").then(
  (res) => console.log(res),
  (err) => console.log(err)
);
```

<details>
  <summary>Solution</summary>
  <pre>
  PromiseGet('https://...')
    .then( res => console.log(res) )
    .catch( err => console.error(err) );
  👉🏻 catch 메서드를 모든 then 메서드를 호출한 이후에 호출하면 비동기 처리에서 발생한 에러(rejected 상태)뿐만 아니라 then메서드 내부에서 발생한 에러까지 보두 캐치한다!
  </pre>
</details>

<br>
